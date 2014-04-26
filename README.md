Dizzy
=====

Dizzy is a wrapper for the DNS Made Easy API in Python.

Requirements
============
You'll need the following:

* [Python 2.7.3](http://www.python.org/)
* [pip](https://github.com/pypa/pip)

Installation
============

```bash
    # Clone the repo
    git clone https://github.com/taeram/dizzy.git ~/.dizzy

    cd ~/.dizzy/

    # Install the dependencies
    sudo pip install -r requirements.txt

    # Add your DNS Made Easy API credentials to your ~/.bashrc
    sudo tee -a ~/.bashrc << EOF
    export DNSMADEEASY_API_KEY=api-key-goes-here
    export DNSMADEEASY_SECRET_KEY=secret-key-goes-here
    EOF

    # Install dizzy
    sudo ln -sf `pwd`/dizzy.py /usr/local/bin/dizzy

    # Voila!
    dizzy
```

Usage
=====

To update the A record for a domain:

```bash
# Usage: dizzy [domain name] update [record name] [IP address]
dizzy example.com update www 127.0.0.1
> www.example.com. 3600 IN A 127.0.0.1
```
