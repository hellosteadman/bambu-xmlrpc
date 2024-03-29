Bambu XML-RPC
=============

An extensible XML-RPC provider

About Bambu XML-RPC
-------------------

This package exposes Python's own XML-RPC functionality to Django views,
and allows any function to work as an XML-RPC endpoint.

About Bambu Tools 2.0
---------------------

This is part of a toolset called Bambu Tools. It's being moved from a
namespace of ``bambu`` to its own 'root-level' package, along with all
the other tools in the set. If you're upgrading from a version prior to
2.0, please make sure to update your code to use ``bambu_xmlrpc`` rather
than ``bambu.xmlrpc``.

Installation
------------

Install the package via Pip:

::

    pip install bambu-xmlrpc

Add it to your ``INSTALLED_APPS`` list:

::

    INSTALLED_APPS = (
        ...
        'bambu_xmlrpc'
    )

Add ``bambu_xmlrpc.urls`` to your URLconf:

::

    urlpatterns = patterns('',
        ...
        url(r'^xml-rpc/', include('bambu_xmlrpc.urls')),
    )

Your endpoint will be available at /xml-rpc/.

Basic usage
-----------

Apply the ``bambu_xmlrpc.handler`` decorator to a function to expose it
as an API. You can then GET from and POST to the function via the
/xml-rpc/ endpoint.

.. automodule:: bambu_xmlrpc
   :members:

Questions or suggestions?
-------------------------

Find me on Twitter (@iamsteadman) or `visit my blog <http://steadman.io/>`_.

Indices and tables
==================

* :ref:`genindex`
* :ref:`modindex`
* :ref:`search`