### Basics
- NGINX has one master process and one or more worker processes
- The worker processes do the actual processing of requests
     - The number is defined by ``` worker_process ```

### Signals
``` nginx -s <Signal> ```
- Where signal is
     - quit (shutdown gracefully)
     - reload (conf file reload) 
     - reopen (reopen log files) [details](https://unix.stackexchange.com/questions/186807/what-does-nginx-s-reopen-do)
     - stop (shutdown immediately)

### Configuration file

#### Directives
- Single line
- Block directives

#### Contexts
Contexts group together the directives that apply to different traffic types
- events (General connection processing)
- http (HTTP traffic)
- mail (Mail traffic)
- stream (TCP and UDP traffic)

#### Virtual servers
Virtual servers are created using ```server``` directive in each context to handle incoming request.