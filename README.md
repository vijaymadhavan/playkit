Playkit: A lightweight bridge api for google playstore
=========================


Usage
------------

    
    >>> from playkit import playkit
    >>> response = playkit.api(keyword="facebook")
    >>> apps = response["results"]
    >>> apps[0]
    >>>{'rating': u'Rated 4.0 stars out of five stars', 'largeImageUrl': u'//lh3.googleusercontent.com/ZZPdzvlpK9r_Df9C3M7j1rNRi7hhHRvPhlklJ3lfi5jk86Jd1s0Y5wcQ1QgbVaAP5Q=w340', 'description': u'  Keeping up with friends is faster than ever.   ', 'price': u'Free', 'smallImageUrl': u'//lh3.googleusercontent.com/ZZPdzvlpK9r_Df9C3M7j1rNRi7hhHRvPhlklJ3lfi5jk86Jd1s0Y5wcQ1QgbVaAP5Q=w170', 'name': u'Facebook', 'id': u'com.facebook.katana', 'developer': u'Facebook'}
  

Installation
------------

To install playkit, simply:


    $ pip install playkit
    ✨🍰✨

