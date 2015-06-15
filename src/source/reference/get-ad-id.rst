.. index:: GET /ad/{id}
.. _get_ad_id:

GET /ad/{id}
============

**Required Scope:** ``api_ro`` or ``console_ro``

This URL returns a single ad with the given ``id``. If the ad does not exist
or does not belong to the user the server returns **404 Not Found**. If the
``id`` is invalid, i.e. not a positive integer the server returns **400 Bad
Request**.

.. note::

    The fields :ref:`ad_pageNumber` and :ref:`ad_suggestedCpcForPageOne` are
    currently expensive to compute. If you do not need their values consider
    excluding them to speed up the response. To exclude the fields add the
    following parameter to the request URL. ::

        ?_exclude=pageNumber,suggestedCpcForPageOne

Parameters
----------

=============    ========    ============================================================================
Name             Type        Description
=============    ========    ============================================================================
_include         string      Comma-separated-list of fields to include. Optional, default is all fields.
_exclude         string      Comma-separated-list of fields to omit. Optional, default empty.
=============    ========    ============================================================================

Errors
------

====================    ====    =======================     ==============================================================================
Field                   Code    Error message               Description
====================    ====    =======================     ==============================================================================
id                      2001    invalid argument            not a valid number
id                      1006    type mismatch               the provided value for the field was not of the correct type
====================    ====    =======================     ==============================================================================

Example
-------

.. include:: ../examples/ad-example.rst