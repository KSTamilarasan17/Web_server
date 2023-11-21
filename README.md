# Developing a Simple Webserver
Name: Tamilarasan
Ref no: 23000080
dept: cyber security
# AIM:

Develop a webserver to display about top five web application development frameworks.

# DESIGN STEPS:

## Step 1:

HTML content creation is done

## Step 2:

Design of webserver workflow

## Step 3:

Implementation using Python code

## Step 4:

Serving the HTML pages.

## Step 5:

Testing the webserver
# PROGRAM:
``````
from http.server import HTTPServer, BaseHTTPRequestHandler

content = """
<html>
<head>
</head>
<body>
<h1>Top Five Web Application development frameworks </h1>
<h2>1.Django<h2>
<h2>2.MEAN stack<h2>
<h2>3.React<h2>
</body>
</html>
class HelloHandler(BaseHTTPRequestHandler):
    def do_GET(self):
        self.send_response(200)
        self.send_header('content-type', 'text/html; charset=utf-8')
        self.end_headers()
        self.wfile.write(content.encode())



server_address = ('', 80)
httpd = HTTPServer(server_address, HelloHandler)
httpd.serve_forever()

``````
# OUTPUT:
![webserver](https://github.com/KSTamilarasan17/Web_server/assets/138849236/b565e748-2bcd-4944-a071-8d6742d3a59a)

# RESULT:

The program is executed succesfully
