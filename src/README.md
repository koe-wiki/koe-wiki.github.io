Infocare Wiki
===

Prerequisites
---
- Install Golang: https://golang.org/dl/
  - Make sure you can call `go` from the command line

- Install Hugo: https://github.com/gohugoio/hugo/releases
  - Make sure you can call `hugo` from the command line

- Install Python 3, recommend also to install `virtualenv`

Setup
---
- Setup Python environment:

  ```bash
  pip install -r requirements.txt
  ```

- Setup hugo-encrypt:
  - Checkout hugo-encrypt here: https://github.com/Izumiko/hugo-encrypt
  - Install hugo-encrypt:
  
    ```bash
    cd hugo-encrypt
    go build
    
    # For Mac/Linux
    sudo mv hugo-encrypt /usr/local/bin
    
    # For windows: copy hugo-encrypt to somewhere and put it on the PATH variable
    ```
  
- Setup SSL certificate:

  ```bash
  openssl req -newkey rsa:2048 -new -nodes -x509 -days 3650 -keyout key.pem -out cert.pem
  ```

Build
---

- Run hugo server during development:

  ```bash
  hugo server
  ```

- To generate static HTML files:

  ```bash
  hugo && hugo-encrypt
  ```
  
  Files will be generated in `public`. Upload the content of this folder to your static host

- To review the encryption:
  
  Generate the files as usual, then:
  
  ```bash
  twistd -no web --path public -c cert.pem -k key.pem --https=8081
  ```

  An HTTPS server will serve `public` content at https://localhost:8081