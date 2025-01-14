- **Deprecated** media type(s): ``application/sellside.ad-v2+json`` ``application/sellside.ad-v3+json``
- New media type: ``application/sellside.ad-v5+json``

- **Price**: ``price`` and ``originalPrice`` map to ``price.amountCents`` and ``price.originalAmountCents`` respectively. The value was already in cents so there is no need for conversion.

- **CPC**: ``cpc`` is replaced by ``bidMicros``, and is represented as a string type, instead of integer. This requires a conversion of the values from a micros unit, when interpreting them as cents.

- **Budget Fields**: ``dailyBudget`` and ``totalBudget`` map to ``budgets.daily.limitMicros`` and ``budgets.total.limitMicros`` respectively. ``dailySpent`` and ``spentBudget`` map to ``budgets.daily.spentMicros`` and ``budgets.total.spentMicros``.
  Values are represented in string type, instead of integer, and at micro precision, instead of cents. The limits can also be ``"UNLIMITED"``.

- **Shipping Cost**: ``cost`` is renamed to ``costCents`` in V5. The value was already in cents so there is no need for conversion.

- **Removed** field(s): ``statusReasons``, ``pageNumber``, ``suggestedCpcForPageOne``, ``currency``, ``allowPayPal``. The field ``vendorId`` should be used instead of ``externalId``, which is deprecated and planned for removal.

- **New** field(s): ``campaignId``: this is an identifier for the campaign which this ad is part of. Campaign management is optional. By default, every seller has one campaign associated with them, with every ad attached to that campaign. See :ref:`campaigns-migration` for more.

- If necessary, position (page number and suggested cost per click) funnel information can be obtained from the replacement `GET /ad/{id}/position <https://ecg-icas.github.io/icas/openapi/index.html#/Ads/getAdPosition>`_ endpoint (see the :ref:`faq-migration`).
