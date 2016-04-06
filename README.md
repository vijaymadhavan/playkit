Playkit: A lightweight bridge api for google playstore
=========================


BasicUsage
------------

    
    >>> from playkit import api
    >>> response = api.search(keyword="facebook")
    >>> apps = response["results"]
    >>> apps[0]
    >>> {'rating': u'Rated 4.0 stars out of five stars', 'largeImageUrl': u'//lh3.googleusercontent.com/ZZPdzvlpK9r_Df9C3M7j1rNRi7hhHRvPhlklJ3lfi5jk86Jd1s0Y5wcQ1QgbVaAP5Q=w340', 
    'description': u'  Keeping up with friends is faster than ever.   ', 
    'price': u'Free', 'smallImageUrl': u'//lh3.googleusercontent.com/ZZPdzvlpK9r_Df9C3M7j1rNRi7hhHRvPhlklJ3lfi5jk86Jd1s0Y5wcQ1QgbVaAP5Q=w170', 
    'name': u'Facebook', 'id': u'com.facebook.katana', 
    'developer': u'Facebook'}
  

Installation
------------

To install playkit, simply:


    $ pip install playkit
    ✨🍰✨

Advanced Usage
------------
#### Category support ####

    >>> response = playkit.api(keyword="facebook",category="apps") # to search apps
    
    >>> response = playkit.api(keyword="facebook",category="books") # to search books
    
#### Pricing ####

    >>> response = playkit.api(keyword="facebook",category="apps",pricing="free") # other values for pricing are "paid" and "all"
    default="all"
    
#### Rating ####

    >>> response = playkit.api(keyword="facebook",category="apps",rating="4+") # rating can also have value "all"
    default="all"
    

#### Proxy support ####
    
    
    >>> proxies = {'http': 'http://10.10.1.10:3128','https': 'http://10.10.1.10:1080'}
    >>> response = playkit.api(keyword="facebook",proxies=proxies)
    
for docs on proxies see [requests](http://docs.python-requests.org/en/master/user/advanced/#proxies)
