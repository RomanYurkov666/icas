.. _ISO 4217: http://en.wikipedia.org/wiki/ISO_4217
.. _ISO 8601: http://en.wikipedia.org/wiki/ISO_8601
.. index:: Categories
.. _categories:
.. _categories_v1:

Categories V1
=============

.. warning::

    Version 1 is deprecated and will be removed at a later point.

The category tree contains all the categories available for placing ads. Each
category has a unique id, a parent id, a label and a list of child categories.
Also, for each category the minimum and maximum cpc values as well as the
minimum and maximum total budgets are specified.

The API allows you to get the entire category tree or just parts of it
depending on your use case. We advise you to get only the parts that you need
at any given moment and not cache the information since it may be subject to
change.

.. include:: examples/category-example-v1.rst

Fields
------

Each ad has a unique identifier by which the ad can retrieved and a set of
required attributes and a set of optional attributes which are listed below:

.. list-table::
 :widths: 5 15 10 70
 :header-rows: 1

 * - Field
   - Example
   - Type
   - Info

 * - id
   - 42
   - int
   - Reference to the Admarkt category

 * - parentId
   - 12
   - int
   - Reference to the parent category

 * - name
   - "Bank"
   - string
   - Display name of the category

 * - currency
   - "EUR"
   - string
   - The `ISO 4217`_ currency code. Currently only *EUR* is supported.
     All Euro amount values are stored in cents

 * - minCpc
   - 10
   - long
   - Minimum CPC value in euro cents for the category

 * - maxCpc
   - 250
   - long
   - Maximum CPC value in euro cents for the category

 * - minTotalBudget
   - 5000
   - long
   - Minimum total budget in euro cents for the category

 * - maxTotalBudget
   - 200000
   - long
   - Maximum total budget in euro cents for the category

 * - minDailyBudget
   - 2000
   - long
   - Minimum daily budget in euro cents for the category

 * - canPlaceAds
   - true
   - bool
   - Flag to indicate whether it is possible to place an ad into this category

 * - maxNumberOfActiveAds
   - 7000
   - int
   - Maximum number of concurrently active ads from the same seller in this category

 * - children
   -
   - list
   - List of child categories

 * - links
   -
   - object
   - Link to the current category and other resources

 * - suggestedCpcForPageOne
   - 152
   - long
   - Suggested cpc value in euro cents for new ads to be on the first page for
     this category. This value is only shown when **canPlaceAds** is true

