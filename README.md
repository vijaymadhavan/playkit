Playkit: A lightweight bridge api for google playstore
=========================


BasicUsage
------------

    
    >>> from playkit import api

    ### App Search Support ###
    >>> response = api.search(keyword="facebook")
    >>> apps = response["results"]
    >>> apps[0]
    >>> {'rating': u'Rated 4.0 stars out of five stars', 'largeImageUrl': u'//lh3.googleusercontent.com/ZZPdzvlpK9r_Df9C3M7j1rNRi7hhHRvPhlklJ3lfi5jk86Jd1s0Y5wcQ1QgbVaAP5Q=w340', 
    'description': u'  Keeping up with friends is faster than ever.   ', 
    'price': u'Free', 'smallImageUrl': u'//lh3.googleusercontent.com/ZZPdzvlpK9r_Df9C3M7j1rNRi7hhHRvPhlklJ3lfi5jk86Jd1s0Y5wcQ1QgbVaAP5Q=w170', 
    'name': u'Facebook', 'id': u'com.facebook.katana', 
    'developer': u'Facebook'}

    ### App Details Support ###
    >>> response = api.appdetails('com.facebook.katana')
    >>> apps = response["results"]
    >>> apps
    >>> {'category': u' Social ', 'rating': u'Rated 4.0 stars out of five stars', 'fileSize': u'  Varies with device ', 'description': u' Keeping up with friends is faster than ever...  ', 'price': 'Free', 'name': u' Facebook ', 'mediumImageUrl': u'//lh3.googleusercontent.com/ZZPdzvlpK9r_Df9C3M7j1rNRi7hhHRvPhlklJ3lfi5jk86Jd1s0Y5wcQ1QgbVaAP5Q=w300', 'currentVersion': u'Varies with device ', 'ratingValue': u'3.975156307220459', 'requiresAndroid': u'Varies with device', 'review': [{'link':u'/store/people/details?id=108065285272182046xxx', 'text': u" A lot better now. It's taken a few years but it's finally becoming the best social media app available.  ", 'title': u'A lot better now.', 'rating': u'Rated 4 stars out of five stars', 'author': u' Bee Lexxx '},...], 'datePublished': u'13 April 2016', 'screenshots': [u'//lh6.ggpht.com/uxLXvxuncWOm2mgU3ChtdGZ0eMp_WJTD4xrVxAKqCJMiR5ibaBbw-VUPJPjcGiqIDRbm=h310',...], 'id': u'com.facebook.katana', 'developer': u' Facebook '}

Installation
------------

To install playkit, simply:


    $ pip install playkit
    ✨🍰✨

Advanced Usage
------------
#### Category support ####

    >>> response = api.search(keyword="facebook",category="apps") # to search apps
    
    >>> response = api.search(keyword="facebook",category="books") # to search books
    
#### Pricing ####

    >>> response = api.search(keyword="facebook",category="apps",pricing="free") # other values for pricing are "paid" and "all"
    default="all"
    
#### Rating ####

    >>> response = api.search(keyword="facebook",category="apps",rating="4+") # rating can also have value "all"
    default="all"
### Country Support ###
    >>> response = api.search(keyword="facebook",category="apps",country="us") # "us" is short for united states 
    default="all"

#### Proxy support ####
    
    
    >>> proxies = {'http': 'http://10.10.1.10:3128','https': 'http://10.10.1.10:1080'}
    >>> response = api.search(keyword="facebook",proxies=proxies)
    
for docs on proxies see [requests](http://docs.python-requests.org/en/master/user/advanced/#proxies)
