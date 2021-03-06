======================
ckanext-tableview
======================

.. Put a description of your extension here:
   What does it do? What features does it have?
   Consider including some screenshots or embedding a video!

Easy to use DataTables plugin in CKAN with different theme to play around with.

Source code for datatables implementation was forked from an official `CKAN Repository <https://github.com/ckan/ckan/tree/ckan-2.8.1/ckanext/datatablesview>`_

.. image:: https://user-images.githubusercontent.com/9320644/95983729-c5408300-0e3f-11eb-9156-d0e2b578bdab.png

------------
Requirements
------------

Tested with CKAN Version 2.6 and 2.8


------------
Installation
------------

.. Add any additional install steps to the list below.
   For example installing any non-Python dependencies or adding any required
   config settings.

To install ckanext-tableview:

1. Activate your CKAN virtual environment, for example::

     . /usr/lib/ckan/default/bin/activate

2. Clone repository and install the ckanext-tableview Python package into your virtual environment::

     python setup.py install

3. Add ``table_view`` to the ``ckan.plugins`` setting in your CKAN
   config file (by default the config file is located at
   ``/etc/ckan/default/production.ini``).

4. Restart CKAN. For example if you've deployed CKAN with Apache on Ubuntu::

     sudo service apache2 reload


-------------
Configuration
-------------

ckanext-tableview has inbuilt themes integrated. To use one, add ``justicehub_theme`` to the ``ckan.tableview_theme`` settings in
your CKAN config file. If not provided, then it will take default theme.
In case if theme is not found, then it will show: "Internal Server Error" in views section


----------------------------
Adding your own custom theme
----------------------------

There are mainly 2 steps for adding any custom theme:

1. Add theme name in ``/tableview/public/resource.config`` along with all the resources you want theme to load
2. Add all relevant css/js files in their respective places inside ``/tableview/public/`` directory anywhere. By default we personally use ``theme`` directory inside ``public`` for custom styles.


------------------------
Development Installation
------------------------

To install ckanext-tableview for development, activate your CKAN virtualenv and
do::

    git clone https://github.com/justicehub-in/ckanext-tableview.git
    cd ckanext-tableview
    python setup.py develop
