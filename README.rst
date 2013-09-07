=====
Django-easy
=====

Django easy is a small Django app that makes creating django views less verbose.


Quick Start
-----------
  pip install django-easy


Usage
----

  # views.py
  from easy.decorators import *

  @context_template_response
  def view_template(request):
    return "home.html"

  @context_template_response
  def view_template_with_vars(request):
    return "home.html", {'vars': 'foobar'}


  @json_response
  def view_simple_json_api(request):
    return {
      'foo': 'bar',
      'numbers': [1, 2, 3]
    }
  
  @string_response
  def view_some_text(request):
    return "hello world!"
