# Best practices: code review, tools, rules, paradigms, design all staff (class, functions, modules), OOP, FP, application architecture, application security.


## Spell checking: definitions, vars, all names (camelCase, etc.)
Mistakes in words, 30 Common Errors & Confusing Words


## Web servers:

    - Stream -> for large peace of data:
        https://flask.palletsprojects.com/en/1.1.x/patterns/streaming/
        https://stackoverflow.com/questions/39272072/flask-send-stream-as-response
        r = requests.get(my_path_to_server01, stream=True)
        return Response(r.iter_content(chunk_size=10*1024), content_type=r.headers['Content-Type'])
    - yield generator


## Sync code

Use Thread/Pool to make async tasks in sync world.
Or use async frameworks.


## Threads:

    - ThreadPoolExecutor
        https://docs.python.org/3.7/library/concurrent.futures.html#concurrent.futures.ThreadPoolExecutor
        https://alexwlchan.net/2019/10/adventures-with-concurrent-futures/
        http://scipy-lectures.org/advanced/advanced_python/index.html


## Requests:

    - stream via microservices:
        with requests.get(URL, stream=True) as r:
            pass
    - timeout:
        res = requests.get(<url>, timeout=10)


## HTTP/status code and REST

    Methods - POST/PUT
    headers - keep-alive
    statuses - 414/202

    https://tools.ietf.org/html/rfc7231    
    https://tools.ietf.org/html/rfc7231#page-48
    https://www.ntu.edu.sg/home/ehchua/programming/webprogramming/HTTP_Basics.html


## RPC
## Message queue

## OS commands:

    https://janakiev.com/blog/python-shell-commands/
    subprocess.run(shell=False) not shell=!True!!
    subprocess.Popen for | (papes)


## Performance and Optimization
    
    https://martinheinz.dev/blog/13


## Memory leaks profiling

    https://docs.python.org/3/library/tracemalloc.html#examples
    https://stackoverflow.com/questions/582336/how-can-you-profile-a-python-script


TODO: 
    
    artificial intelligence for code review with own DB of prediction and best practices.
