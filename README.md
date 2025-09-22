# Name:JAIRAM J.
# Date:22-09-2025




# EX01 Developing a Simple Webserver

## AIM:
To develop a simple webserver to serve html pages.

## DESIGN STEPS:

### Step 1: 
HTML content creation.

### Step 2:
Design of webserver workflow.

### Step 3:
Implementation using Python code.

### Step 4:
Serving the HTML pages.

### Step 5:
Testing the webserver.


## PROGRAM:
```
from http.server import HTTPServer, BaseHTTPRequestHandler
content = """
<html>
     <title> Software Companies Revenue </title>
     <body>
           <table border = "2" cellspacing = "10" cellpading = "6">
              <caption>TOP SIX REVENUE SOFTWARE COMPANIES </caption>
              <tr>
                  <th>S.NO</th>
                  <th>COMPANY</th>			
                  <th>REVENUE</th>
              </tr>
              <tr>
                  <td>1</td>
                  <td>Microsoft</td>
                  <td>65 Billion</td>
             </tr>
             <tr>
                  <td>2</td>
                  <td>Oracle</td>
                  <td>29.6 Billion</td>
             </tr>
             <tr>
                  <td>3</td>
                  <td>IBM</td>
                  <td>29.1Billion</td>
            </tr>
            <tr>
                  <td>4</td>
                  <td>SAP</td>
                  <td>6.4 Billion</td>
            </tr>
            <tr>
                  <td>5</td>
                  <td>Symantic</td>
                  <td>5.6 Billion</td>
            </tr>
            <tr>
                <td>6</td>
                <td>Adobe Inc</td>
                <td>19.8 Billion</td>
          </tr>
           
            
        

       </table>
    </body>
</html>
"""
class myhandler(BaseHTTPRequestHandler):
    def do_GET(self):
        print("request received")
        self.send_response(200)
        self.send_header('content-type', 'text/html; charset=utf-8')
        self.end_headers()
        self.wfile.write(content.encode())
server_address = ('',8000)
httpd = HTTPServer(server_address,myhandler)
print("my webserver is running...")
httpd.serve_forever()

```

## OUTPUT:

<img width="1918" height="997" alt="364058258-81b12071-0755-4809-9c6c-b5d7f7ba1d42" src="https://github.com/user-attachments/assets/74fa6db1-5987-406c-8292-e45ad8362bc4" />





## RESULT:
The program for implementing simple webserver is executed successfully.
