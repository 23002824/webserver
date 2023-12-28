# Developing a Simple Webserver

# AIM:

To develop a simple webserver to serve html programming pages.

## DESIGN STEPS:

### Step 1:

HTML content creation is done

### Step 2:

Design of webserver workflow

### Step 3:

Implementation using Python code

### Step 4:

Serving the HTML pages.

### Step 5:

Testing the webserver

## PROGRAM:
```
from http.server import HTTPServer, BaseHTTPRequestHandler

content="""

<html>
<head>
</head>
<body>
<h1>Welcome</h1>
</body>
</html>
"""

class MyHandler(BaseHTTPRequestHandler):
    def do_GET(self):
        self.send_response(200)
        self.send_header('Content-type', 'text/html')
        self.end_headers()
        self.wfile.write(content.encode())


server_address=('',80)
httpd=HTTPServer(server_address,HelloHandler)
httpd.serve_forever()

```

## OUTPUT:
![Screenshot 2023-12-28 110650](https://github.com/23002824/webserver/assets/151514009/33281de1-8476-4d51-b84d-80c05c4be0a9)


## RESULT:
The program is executed succesfully
