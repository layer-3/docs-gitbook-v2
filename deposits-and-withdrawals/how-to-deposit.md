---
description: 'TODO: add page description'
---

# How to Deposit

{% hint style="info" %}
**Placeholder — structure only.**

**What to cover:** External Wallet tab: direct deposit + approval-vs-deposit transactions. Gmail tab: two-step flow (funds land in Account Balance first). Include asset/network warnings.

**Tabs are required — do not merge the flows.** The External Wallet and Gmail deposit flows differ, so they MUST stay in separate GitBook tabs (not one combined prose block, not two separate pages). Keep the `{% tabs %}` block below and write each flow inside its own `{% tab %}`. GitBook syntax:

````
{% tabs %}
{% tab title="External Wallet" %}
...flow for connected-wallet users...
{% endtab %}

{% tab title="Gmail / Email Account" %}
...flow for Gmail/email users...
{% endtab %}
{% endtabs %}
````

**Source:** Merge of external-wallet + gmail deposit + approval-vs-deposit + two-step flow. Migrate: v1 fund-your-account.md, quick-start.md
{% endhint %}

{% tabs %}
{% tab title="External Wallet" %}
TODO: direct deposit flow from a connected wallet; include the approval vs deposit transaction distinction.
{% endtab %}

{% tab title="Gmail / Email Account" %}
TODO: two-step deposit flow — funds arrive in Account Balance first, then transfer to Trading Account.
{% endtab %}
{% endtabs %}
