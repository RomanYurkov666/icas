- **Deprecated** media type(s): ``application/sellside.category-v2+json``
- New media type: ``application/sellside.category-v5+json``
- **CPC**: `cpc` is replaced by ``bidMicros``. The interval values require conversion from a micros unit when interpreting them as cents.
- **Budget Fields**: ``dailyBudget`` and ``totalBudget`` map to ``dailyBudgetMicros`` and ``totalBudgetMicros`` respectively. The interval values require conversion from a micros unit, when interpreting them as cents.
- **Removed** field(s): ``suggestedCpcForPageOne``, ``currency``, ``paypalEnabled``.