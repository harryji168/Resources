 
## Stripe API reference
 

https://stripe.com/docs/api

[Docs](/docs)

[Support](/support)

[Sign in →](https://dashboard.stripe.com/login?redirect=https%3A%2F%2Fstripe.com%2Fdocs%2Fapi%2Fsources)

API Reference
=============

The Stripe API is organized around [REST](http://en.wikipedia.org/wiki/Representational_State_Transfer). Our API has predictable resource-oriented URLs, accepts [form-encoded](https://en.wikipedia.org/wiki/POST_(HTTP)#Use_for_submitting_web_forms) request bodies, returns [JSON-encoded](http://www.json.org/) responses, and uses standard HTTP response codes, authentication, and verbs.

You can use the Stripe API in test mode, which does not affect your live data or interact with the banking networks. The API key you use to [authenticate](#authentication) the request determines whether the request is live mode or test mode.

The Stripe API differs for every account as we release new [versions](#versioning) and tailor functionality. Log in to see docs customized to your version of the API, with your test key and data.

Was this section helpful?YesNo

Just getting started?

Check out our [development quickstart](/docs/development/quickstart) guide.

Not a developer?

Use apps from [our partners](/works-with/type/platform) to get started with Stripe and to do more with your Stripe account—no code required.

Base URL

    https://api.stripe.com

Client libraries

[

Ruby

](/docs/api/sources?lang=ruby)[

Python

](/docs/api/sources?lang=python)[

PHP

](/docs/api/sources?lang=php)[

Java

](/docs/api/sources?lang=java)[

Node.js

](/docs/api/sources?lang=node)[

Go

](/docs/api/sources?lang=go)[

.NET

](/docs/api/sources?lang=dotnet)

By default, the Stripe API Docs demonstrate using curl to interact with the API over HTTP. Select one of our official [client libraries](https://stripe.com/docs/libraries) to see examples in code.

Authentication
==============

The Stripe API uses [API keys](/docs/keys) to authenticate requests. You can view and manage your API keys in [the Stripe Dashboard](/login?redirect=/account/apikeys).

Test mode secret keys have the prefix `sk_test_` and live mode secret keys have the prefix `sk_live_`. Alternatively, you can use [restricted API keys](/docs/keys#limiting-access-with-restricted-api-keys) for granular permissions.

Your API keys carry many privileges, so be sure to keep them secure! Do not share your secret API keys in publicly accessible areas such as GitHub, client-side code, and so forth.

Authentication to the API is performed via [HTTP Basic Auth](http://en.wikipedia.org/wiki/Basic_access_authentication). Provide your API key as the basic auth username value. You do not need to provide a password.

If you need to authenticate via bearer auth (e.g., for a cross-origin request), use `-H "Authorization: Bearer sk_test_4eC39HqLyjWDarjtT1zdp7dc"` instead of `-u sk_test_4eC39HqLyjWDarjtT1zdp7dc`.

All API requests must be made over [HTTPS](http://en.wikipedia.org/wiki/HTTP_Secure). Calls made over plain HTTP will fail. API requests without authentication will also fail.

Related video: [Authentication](https://www.youtube.com/watch?v=8Db0nTVlKM0&list=PLy1nL-pvL2M50RmP6ie-gdcSnfOuQCRYk).

Was this section helpful?YesNo

Authenticated Request

Select librarycURLStripe CLIRubyPythonPHPJavaNode.jsGo.NET

1

2

3

    curl https://api.stripe.com/v1/charges \
      -u sk_test_4eC39HqLyjWDarjtT1zdp7dc:
    # The colon prevents curl from asking for a password.

Your API Key

A sample test API key is included in all the examples here, so you can test any example right away. Do not submit any personally identifiable information in requests made with this key.

To test requests using your account, replace the sample API key with your actual API key or [sign in](/login?redirect=https%3A%2F%2Fstripe.com%2Fdocs%2Fapi%2Fsources).

Connected Accounts
==================

Clients can make requests as connected accounts using the special header `Stripe-Account` which should contain a Stripe account ID (usually starting with the prefix `acct_`).

See also [Making API calls for connected accounts](/docs/connect/authentication).

Was this section helpful?YesNo

Per-request account

Select librarycURLStripe CLIRubyPythonPHPJavaNode.jsGo.NET

1

2

3

4

    curl https://api.stripe.com/v1/charges/ch_3KIQAp2eZvKYlo2C0E0dCQHx \
      -u sk_test_4eC39HqLyjWDarjtT1zdp7dc: \
      -H "Stripe-Account: acct_1032D82eZvKYlo2C" \
      -G

Errors
======

Stripe uses conventional HTTP response codes to indicate the success or failure of an API request. In general: Codes in the `2xx` range indicate success. Codes in the `4xx` range indicate an error that failed given the information provided (e.g., a required parameter was omitted, a charge failed, etc.). Codes in the `5xx` range indicate an error with Stripe's servers (these are rare).

Some `4xx` errors that could be handled programmatically (e.g., a card is [declined](/docs/declines)) include an [error code](/docs/error-codes) that briefly explains the error reported.

Was this section helpful?YesNo

##### Attributes

*   ### [
    
    ](#errors-type)type string
    
    The type of error returned. One of `api_error`, `card_error`, `idempotency_error`, or `invalid_request_error`
    
*   ### [
    
    ](#errors-code)code string
    
    For some errors that could be handled programmatically, a short string indicating the [error code](/docs/error-codes) reported.
    
*   ### [
    
    ](#errors-decline_code)decline\_code string
    
    For card errors resulting from a card issuer decline, a short string indicating the [card issuer’s reason for the decline](/docs/declines#issuer-declines) if they provide one.
    
*   ### [
    
    ](#errors-message)message string
    
    A human-readable message providing more details about the error. For card errors, these messages can be shown to your users.
    
*   ### [
    
    ](#errors-param)param string
    
    If the error is parameter-specific, the parameter related to the error. For example, you can use this to display a message near the correct form field.
    
*   ### [
    
    ](#errors-payment_intent)payment\_intent hash
    
    The PaymentIntent object for errors returned on a request involving a PaymentIntent.
    
    ##### Show child attributes
    

##### More attributesExpand all

*   ### [
    
    ](#errors-charge)
    
    charge string
    
*   ### [
    
    ](#errors-doc_url)
    
    doc\_url string
    
*   ### [
    
    ](#errors-payment_method)
    
    payment\_method hash
    
*   ### [
    
    ](#errors-payment_method_type)
    
    payment\_method\_type string
    
*   ### [
    
    ](#errors-setup_intent)
    
    setup\_intent hash
    
*   ### [
    
    ](#errors-source)
    
    source hash
    

HTTP status code summary

200 - OK

Everything worked as expected.

400 - Bad Request

The request was unacceptable, often due to missing a required parameter.

401 - Unauthorized

No valid API key provided.

402 - Request Failed

The parameters were valid but the request failed.

403 - Forbidden

The API key doesn't have permissions to perform the request.

404 - Not Found

The requested resource doesn't exist.

409 - Conflict

The request conflicts with another request (perhaps due to using the same idempotent key).

429 - Too Many Requests

Too many requests hit the API too quickly. We recommend an exponential backoff of your requests.

500, 502, 503, 504 - Server Errors

Something went wrong on Stripe's end. (These are rare.)

Error types

api\_error

API errors cover any other type of problem (e.g., a temporary problem with Stripe's servers), and are extremely uncommon.

card\_error

Card errors are the most common type of error you should expect to handle. They result when the user enters a card that can't be charged for some reason.

idempotency\_error

Idempotency errors occur when an `Idempotency-Key` is re-used on a request that does not match the first request's API endpoint and parameters.

invalid\_request\_error

Invalid request errors arise when your request has invalid parameters.

Handling errors
===============

Our Client libraries raise exceptions for many reasons, such as a failed charge, invalid parameters, authentication errors, and network unavailability. We recommend writing code that gracefully handles all possible API exceptions.

Related guide: [Error Handling](/docs/error-handling).

Select librarycURLStripe CLIRubyPythonPHPJavaNode.jsGo.NET

1

    # Select a client library to see examples of handling different kinds of errors.

Expanding Responses
===================

Many objects allow you to request additional information as an expanded response by using the `expand` request parameter. This parameter is available on all API requests, and applies to the response of that request only. Responses can be expanded in two ways.

In many cases, an object contains the ID of a related object in its response properties. For example, a `Charge` may have an associated `Customer` ID. Those objects can be expanded inline with the `expand` request parameter. ID fields that can be expanded into objects are noted in this documentation with the`expandable` label.

In some cases, such as the Issuing Card object's `number` and `cvc` fields, there are available fields that are not included in responses by default. You can request these fields as an expanded response by using the `expand` request parameter. Fields that can be included in an expanded response are noted in this documentation with the `expandable` label.

You can expand recursively by specifying nested fields after a dot (`.`). For example, requesting `invoice.subscription` on a charge will expand the `invoice` property into a full Invoice object, and will then expand the `subscription` property on that invoice into a full Subscription object.

You can use the `expand` param on any endpoint which returns expandable fields, including list, create, and update endpoints.

Expansions on list requests start with the `data` property. For example, you would expand `data.customers` on a request to list charges and associated customers. Many deep expansions on list requests can be slow.

Expansions have a maximum depth of four levels (so for example, when listing charges,`data.invoice.subscription.default_source` is the deepest allowed).

You can expand multiple objects at once by identifying multiple items in the `expand` array.

Related Guide: [Expanding responses](/docs/expand)

Related video: [Expand](https://www.youtube.com/watch?v=dkpknsaWuQQ&list=PLy1nL-pvL2M50RmP6ie-gdcSnfOuQCRYk&index=8).

Was this section helpful?YesNo

Charge with expanded customer, invoice, and subscription

Select librarycURLStripe CLIRubyPythonPHPJavaNode.jsGo.NET

1

2

3

4

5

    curl https://api.stripe.com/v1/charges/ch_3KIQAp2eZvKYlo2C0E0dCQHx \
      -u sk_test_4eC39HqLyjWDarjtT1zdp7dc: \
      -d "expand[]"=customer \
      -d "expand[]"="invoice.subscription" \
      -G

Response

    {
      "id": "ch_3KIQAp2eZvKYlo2C0E0dCQHx",
      "object": "charge",
      "customer": {
        "id": "cu_19yUki2eZvKYlo2CU3qecbj3",
        "object": "customer",
        ...
      },
      "invoice": {
        "id": "in_1KIQAp2eZvKYlo2CT0Dp70AJ",
        "object": "invoice",
        "subscription": {
          "id": "su_1JedxM2eZvKYlo2C7PQRnJiD",
          "object": "subscription",
          ...
        },
        ...
      },
      ...
    }

Idempotent Requests
===================

The API supports [idempotency](https://en.wikipedia.org/wiki/Idempotence) for safely retrying requests without accidentally performing the same operation twice. This is useful when an API call is disrupted in transit and you do not receive a response. For example, if a request to [create a charge](#create_charge) does not respond due to a network connection error, you can retry the request with the same idempotency key to guarantee that no more than one charge is created.

To perform an idempotent request, provide an additional `Idempotency-Key: <key>` header to the request.

Stripe's idempotency works by saving the resulting status code and body of the first request made for any given idempotency key, regardless of whether it succeeded or failed. Subsequent requests with the same key return the same result, including `500` errors.

An idempotency key is a unique value generated by the client which the server uses to recognize subsequent retries of the same request. How you create unique keys is up to you, but we suggest using V4 UUIDs, or another random string with enough entropy to avoid collisions. Idempotency keys can be up to 255 characters long.

Keys are eligible to be removed from the system automatically after they're at least 24 hours old, and a new request is generated if a key is reused after the original has been pruned. The idempotency layer compares incoming parameters to those of the original request and errors unless they're the same to prevent accidental misuse.

Results are only saved if an API endpoint started executing. If incoming parameters failed validation, or the request conflicted with another that was executing concurrently, no idempotent result is saved because no API endpoint began execution. It is safe to retry these requests.

All `POST` requests accept idempotency keys. Sending idempotency keys in `GET` and `DELETE` requests has no effect and should be avoided, as these requests are idempotent by definition.

Related video: [Idempotency and retries](https://www.youtube.com/watch?v=nnMqSQtSZUQ&list=PLy1nL-pvL2M50RmP6ie-gdcSnfOuQCRYk&index=6).

Was this section helpful?YesNo

Select librarycURLStripe CLIRubyPythonPHPJavaNode.jsGo.NET

1

2

3

4

5

6

7

    curl https://api.stripe.com/v1/charges \
      -u sk_test_4eC39HqLyjWDarjtT1zdp7dc: \
      -H "Idempotency-Key: j7pWyBeqQD6ewaIb" \
      -d amount=2000 \
      -d currency=usd \
      -d description="My First Test Charge (created for API docs)" \
      -d source=tok_mastercard

Metadata
========

Updateable Stripe objects—including [Account](#account), [Charge](#charges), [Customer](#customers), [PaymentIntent](#payment_intents), [Refund](#refunds), [Subscription](#subscriptions), and [Transfer](#transfers)—have a `metadata` parameter. You can use this parameter to attach key-value data to these Stripe objects.

You can specify up to 50 keys, with key names up to 40 characters long and values up to 500 characters long.

Metadata is useful for storing additional, structured information on an object. As an example, you could store your user's full name and corresponding unique identifier from your system on a Stripe [Customer](#customers) object. Metadata is not used by Stripe—for example, not used to authorize or decline a charge—and won't be seen by your users unless you choose to show it to them.

Some of the objects listed above also support a `description` parameter. You can use the `description` parameter to annotate a charge—with, for example, a human-readable description like `2 shirts for test@example.com`. Unlike `metadata`, `description` is a single string, and your users may see it (e.g., in email receipts Stripe sends on your behalf).

Do not store any sensitive information (bank account numbers, card details, etc.) as metadata or in the `description` parameter.

Related video: [Metadata](https://www.youtube.com/watch?v=fPYi0y2LSDQ&list=PLy1nL-pvL2M50RmP6ie-gdcSnfOuQCRYk&index=4).

Was this section helpful?YesNo

##### Sample metadata use cases

*   ### Link IDs
    
    Attach your system's unique IDs to a Stripe object, for easy lookups. For example, add your order number to a charge, your user ID to a customer or recipient, or a unique receipt number to a transfer.
    
*   ### Refund papertrails
    
    Store information about why a refund was created, and by whom.
    
*   ### Customer details
    
    Annotate a customer by storing an internal ID for your later use.
    

Select librarycURLStripe CLIRubyPythonPHPJavaNode.jsGo.NET

1

2

3

4

5

6

    curl https://api.stripe.com/v1/charges \
      -u sk_test_4eC39HqLyjWDarjtT1zdp7dc: \
      -d amount=2000 \
      -d currency=usd \
      -d source=tok_mastercard \
      -d "metadata[order_id]"=6735

Response

    {
      "id": "ch_3KIQAp2eZvKYlo2C0E0dCQHx",
      "object": "charge",
      "amount": 100,
      "amount_captured": 0,
      "amount_refunded": 0,
      "application": null,
      "application_fee": null,
      "application_fee_amount": null,
      "balance_transaction": "txn_1032HU2eZvKYlo2CEPtcnUvl",
      "billing_details": {
        "address": {
          "city": null,
          "country": null,
          "line1": null,
          "line2": null,
          "postal_code": null,
          "state": null
        },
        "email": null,
        "name": null,
        "phone": null
      },
      "calculated_statement_descriptor": null,
      "captured": false,
      "created": 1642306619,
      "currency": "usd",
      "customer": null,
      "description": "My First Test Charge (created for API docs)",
      "disputed": false,
      "failure_code": null,
      "failure_message": null,
      "fraud_details": {},
      "invoice": null,
      "livemode": false,
      "metadata": {
        "order_id": "6735"
      },
      "on_behalf_of": null,
      "order": null,
      "outcome": null,
      "paid": true,
      "payment_intent": null,
      "payment_method": "card_19yUki2eZvKYlo2CuyjKebGi",
      "payment_method_details": {
        "card": {
          "brand": "visa",
          "checks": {
            "address_line1_check": null,
            "address_postal_code_check": null,
            "cvc_check": null
          },
          "country": "CA",
          "exp_month": 3,
          "exp_year": 2018,
          "fingerprint": "CzzwE1ax7qiHgw16",
          "funding": "credit",
          "installments": null,
          "last4": "1881",
          "network": "visa",
          "three_d_secure": null,
          "wallet": null
        },
        "type": "card"
      },
      "receipt_email": null,
      "receipt_number": null,
      "receipt_url": "https://pay.stripe.com/receipts/acct_1032D82eZvKYlo2C/ch_3KIQAp2eZvKYlo2C0E0dCQHx/rcpt_KyMuzICKWGvpkZIZlK72cQlRGC8bysg",
      "refunded": false,
      "refunds": {
        "object": "list",
        "data": [],
        "has_more": false,
        "url": "/v1/charges/ch_3KIQAp2eZvKYlo2C0E0dCQHx/refunds"
      },
      "review": null,
      "shipping": null,
      "source_transfer": null,
      "statement_descriptor": null,
      "statement_descriptor_suffix": null,
      "status": "succeeded",
      "transfer_data": null,
      "transfer_group": null
    }

Pagination
==========

All top-level API resources have support for bulk fetches via "list" API methods. For instance, you can [list charges](#list_charges), [list customers](#list_customers), and [list invoices](#list_invoices). These list API methods share a common structure, taking at least these three parameters: `limit`, `starting_after`, and `ending_before`.

Stripe utilizes cursor-based pagination via the `starting_after` and `ending_before` parameters. Both parameters take an existing object ID value (see below) and return objects in reverse chronological order. The `ending_before` parameter returns objects listed before the named object. The `starting_after` parameter returns objects listed after the named object. These parameters are mutually exclusive -- only one of `starting_after` or`ending_before` may be used.

Our client libraries offer [auto-pagination](#auto_pagination) helpers to easily traverse all pages of a list.

Related video: [Pagination and auto-pagination](https://www.youtube.com/watch?v=mawDqjFzTIQ&list=PLy1nL-pvL2M50RmP6ie-gdcSnfOuQCRYk).

Was this section helpful?YesNo

##### Parameters

*   ### [
    
    ](#pagination-limit)limit optional, default is 10
    
    A limit on the number of objects to be returned, between 1 and 100.
    
*   ### [
    
    ](#pagination-starting_after)starting\_after optional
    
    A cursor for use in pagination. `starting_after` is an object ID that defines your place in the list. For instance, if you make a list request and receive 100 objects, ending with `obj_foo`, your subsequent call can include `starting_after=obj_foo` in order to fetch the next page of the list.
    
*   ### [
    
    ](#pagination-ending_before)ending\_before optional
    
    A cursor for use in pagination. `ending_before` is an object ID that defines your place in the list. For instance, if you make a list request and receive 100 objects, starting with `obj_bar`, your subsequent call can include `ending_before=obj_bar` in order to fetch the previous page of the list.
    

##### List Response Format

*   ### [
    
    ](#pagination-object)object string, value is "list"
    
    A string describing the object type returned.
    
*   ### [
    
    ](#pagination-data)data array
    
    An array containing the actual response elements, paginated by any request parameters.
    
*   ### [
    
    ](#pagination-has_more)has\_more boolean
    
    Whether or not there are more elements available after this set. If `false`, this set comprises the end of the list.
    
*   ### [
    
    ](#pagination-url)url string
    
    The URL for accessing this list.
    

Response

    {
      "object": "list",
      "url": "/v1/customers",
      "has_more": false,
      "data": [
        {
          "id": "cus_AJ6yY15pe9xOZe",
          "object": "customer",
          "address": null,
          "balance": 0,
          "created": 1489794300,
          "currency": "usd",
          "default_source": "card_19yUki2eZvKYlo2CuyjKebGi",
          "delinquent": true,
          "description": "Sample user",
          "discount": null,
          "email": "brennon.monahan@example.com",
          "invoice_prefix": "2F32A58",
          "invoice_settings": {
            "custom_fields": null,
            "default_payment_method": null,
            "footer": null
          },
          "livemode": false,
          "metadata": {
            "order_id": "6735"
          },
          "name": null,
          "next_invoice_sequence": 99656,
          "phone": null,
          "preferred_locales": [],
          "shipping": null,
          "tax_exempt": "none"
        },
        {...},
        {...}
      ]
    }

Auto-pagination
===============

Our libraries support auto-pagination. This feature easily handles fetching large lists of resources without having to manually paginate results and perform subsequent requests.

Since curl simply emits raw HTTP requests, it doesn't support auto-pagination.

Select librarycURLStripe CLIRubyPythonPHPJavaNode.jsGo.NET

1

2

    # The auto-pagination feature is specific to Stripe's
      # libraries and cannot be used directly with curl.

Request IDs
===========

Each API request has an associated request identifier. You can find this value in the response headers, under `Request-Id`. You can also find request identifiers in the URLs of individual request logs in your [Dashboard](https://dashboard.stripe.com/logs). **If you need to contact us about a specific request, providing the request identifier will ensure the fastest possible resolution.**

Was this section helpful?YesNo

Select librarycURLStripe CLIRubyPythonPHPJavaNode.jsGo.NET

1

2

3

4

    curl https://api.stripe.com/v1/customers \
      -u sk_test_4eC39HqLyjWDarjtT1zdp7dc: \
      -D "-" \
      -X POST

Versioning
==========

When [backwards-incompatible](/docs/upgrades#what-changes-does-stripe-consider-to-be-backwards-compatible) changes are made to the API, a new, dated version is released. The current version is **2020-08-27**. Read our [API upgrades guide](/docs/upgrades) to see our [API changelog](/docs/upgrades#api-changelog) and to learn more about backwards compatibility.

All requests use your account API settings, unless you override the API version. The [changelog](/docs/upgrades#api-changelog) lists every available version. _Note that by default webhook events are structured according to your account API version, unless you set an API version during [endpoint creation](/docs/api/webhook_endpoints/create)._

To set the API version on a specific request, send a `Stripe-Version` header.

You can visit [your Dashboard](https://dashboard.stripe.com/developers) to upgrade your API version. As a precaution, use API versioning to test a new API version before committing to an upgrade.

Related video: [Versioning](https://www.youtube.com/watch?v=PxMztPi6q6Q&list=PLy1nL-pvL2M50RmP6ie-gdcSnfOuQCRYk).

Was this section helpful?YesNo

Select librarycURLStripe CLIRubyPythonPHPJavaNode.jsGo.NET

1

2

3

    curl https://api.stripe.com/v1/charges \
      -u sk_test_4eC39HqLyjWDarjtT1zdp7dc: \
      -H "Stripe-Version: 2020-08-27"

Balance
=======

This is an object representing your Stripe balance. You can retrieve it to see the balance currently on your Stripe account…

Endpoints

 [GET 

    /v1/balance](#retrieve_balance)

Show

Balance Transactions
====================

Balance transactions represent funds moving through your Stripe account. They're created for every type of transaction that comes into or flows out of your Stripe account balance…

Endpoints

 [GET 

    /v1/balance_transactions/:id](#balance_transaction_retrieve)

 [GET 

    /v1/balance_transactions](#balance_transaction_list)

Show

Charges
=======

To charge a credit or a debit card, you create a `Charge` object. You can retrieve and refund individual charges as well as list all charges. Charges are identified by a unique, random ID…

Endpoints

 [POST 

    /v1/charges](#create_charge)

 [GET 

    /v1/charges/:id](#retrieve_charge)

 [POST 

    /v1/charges/:id](#update_charge)

 [POST 

    /v1/charges/:id/capture](#capture_charge)

 [GET 

    /v1/charges](#list_charges)

Show

Customers
=========

This object represents a customer of your business. It lets you create recurring charges and track payments that belong to the same customer…

Endpoints

 [POST 

    /v1/customers](#create_customer)

 [GET 

    /v1/customers/:id](#retrieve_customer)

 [POST 

    /v1/customers/:id](#update_customer)

[

    DELETE 

    /v1/customers/:id





](#delete_customer)

 [GET 

    /v1/customers](#list_customers)

Show

Disputes
========

A dispute occurs when a customer questions your charge with their card issuer. When this happens, you're given the opportunity to respond to the dispute with evidence that shows that the charge is legitimate. You can find more information about the dispute process in our [Disputes and Fraud](/docs/disputes) documentation…

Endpoints

 [GET 

    /v1/disputes/:id](#retrieve_dispute)

 [POST 

    /v1/disputes/:id](#update_dispute)

 [POST 

    /v1/disputes/:id/close](#close_dispute)

 [GET 

    /v1/disputes](#list_disputes)

Show

Events
======

Events are our way of letting you know when something interesting happens in your account. When an interesting event occurs, we create a new `Event` object. For example, when a charge succeeds, we create a `charge.succeeded` event; and when an invoice payment attempt fails, we create an `invoice.payment_failed` event. Note that many API requests may cause multiple events to be created. For example, if you create a new subscription for a customer, you will receive both a `customer.subscription.created` event and a `charge.succeeded` event…

Endpoints

 [GET 

    /v1/events/:id](#retrieve_event)

 [GET 

    /v1/events](#list_events)

Show

Files
=====

This is an object representing a file hosted on Stripe's servers. The file may have been uploaded by yourself using the [create file](#create_file) request (for example, when uploading dispute evidence) or it may have been created by Stripe (for example, the results of a [Sigma scheduled query](#scheduled_queries))…

Endpoints

 [POST 

    https://files.stripe.com/v1/files](#create_file)

 [GET 

    /v1/files/:id](#retrieve_file)

 [GET 

    /v1/files](#list_files)

Show

File Links
==========

To share the contents of a `File` object with non-Stripe users, you can create a `FileLink`. `FileLink`s contain a URL that can be used to retrieve the contents of the file without authentication.

Endpoints

 [POST 

    /v1/file_links](#create_file_link)

 [GET 

    /v1/file_links/:id](#retrieve_file_link)

 [POST 

    /v1/file_links/:id](#update_file_link)

 [GET 

    /v1/file_links](#list_file_links)

Show

Mandates
========

A Mandate is a record of the permission a customer has given you to debit their payment method.

Endpoints

 [GET 

    /v1/mandates/:id](#retrieve_mandate)

Show

PaymentIntents
==============

A PaymentIntent guides you through the process of collecting a payment from your customer. We recommend that you create exactly one PaymentIntent for each order or customer session in your system. You can reference the PaymentIntent later to see the history of payment attempts for a particular session…

Endpoints

 [POST 

    /v1/payment_intents](#create_payment_intent)

 [GET 

    /v1/payment_intents/:id](#retrieve_payment_intent)

 [POST 

    /v1/payment_intents/:id](#update_payment_intent)

 [POST 

    /v1/payment_intents/:id/confirm](#confirm_payment_intent)

 [POST 

    /v1/payment_intents/:id/capture](#capture_payment_intent)

 [POST 

    /v1/payment_intents/:id/cancel](#cancel_payment_intent)

 [GET 

    /v1/payment_intents](#list_payment_intents)

Show

SetupIntents
============

A SetupIntent guides you through the process of setting up and saving a customer's payment credentials for future payments. For example, you could use a SetupIntent to set up and save your customer's card without immediately collecting a payment. Later, you can use [PaymentIntents](#payment_intents) to drive the payment flow…

Endpoints

 [POST 

    /v1/setup_intents](#create_setup_intent)

 [GET 

    /v1/setup_intents/:id](#retrieve_setup_intent)

 [POST 

    /v1/setup_intents/:id](#update_setup_intent)

 [POST 

    /v1/setup_intents/:id/confirm](#confirm_setup_intent)

 [POST 

    /v1/setup_intents/:id/cancel](#cancel_setup_intent)

 [GET 

    /v1/setup_intents](#list_setup_intents)

Show

SetupAttempts
=============

A SetupAttempt describes one attempted confirmation of a SetupIntent, whether that confirmation was successful or unsuccessful. You can use SetupAttempts to inspect details of a specific attempt at setting up a payment method using a SetupIntent.

Endpoints

 [GET 

    /v1/setup_attempts](#list_setup_attempts)

Show

Payouts
=======

A `Payout` object is created when you receive funds from Stripe, or when you initiate a payout to either a bank account or debit card of a [connected Stripe account](/docs/connect/bank-debit-card-payouts). You can retrieve individual payouts, as well as list all payouts. Payouts are made on [varying schedules](/docs/connect/manage-payout-schedule), depending on your country and industry…

Endpoints

 [POST 

    /v1/payouts](#create_payout)

 [GET 

    /v1/payouts/:id](#retrieve_payout)

 [POST 

    /v1/payouts/:id](#update_payout)

 [GET 

    /v1/payouts](#list_payouts)

 [POST 

    /v1/payouts/:id/cancel](#cancel_payout)

 [POST 

    /v1/payouts/:id/reverse](#reverse_payout)

Show

Refunds
=======

`Refund` objects allow you to refund a charge that has previously been created but not yet refunded. Funds will be refunded to the credit or debit card that was originally charged…

Endpoints

 [POST 

    /v1/refunds](#create_refund)

 [GET 

    /v1/refunds/:id](#retrieve_refund)

 [POST 

    /v1/refunds/:id](#update_refund)

 [GET 

    /v1/refunds](#list_refunds)

Show

Tokens
======

Tokenization is the process Stripe uses to collect sensitive card or bank account details, or personally identifiable information (PII), directly from your customers in a secure manner. A token representing this information is returned to your server to use. You should use our [recommended payments integrations](/docs/payments) to perform this process client-side. This ensures that no sensitive card data touches your server, and allows your integration to operate in a PCI-compliant way…

Endpoints

 [POST 

    /v1/tokens](#create_card_token)

 [POST 

    /v1/tokens](#create_bank_account_token)

 [POST 

    /v1/tokens](#create_pii_token)

 [POST 

    /v1/tokens](#create_account_token)

 [POST 

    /v1/tokens](#create_person_token)

 [POST 

    /v1/tokens](#create_cvc_update_token)

 [GET 

    /v1/tokens/:id](#retrieve_token)

Show

PaymentMethods
==============

PaymentMethod objects represent your customer's payment instruments. They can be used with [PaymentIntents](/docs/payments/payment-intents) to collect payments or saved to Customer objects to store instrument details for future payments…

Endpoints

 [POST 

    /v1/payment_methods](#create_payment_method)

 [GET 

    /v1/payment_methods/:id](#retrieve_payment_method)

 [POST 

    /v1/payment_methods/:id](#update_payment_method)

 [GET 

    /v1/payment_methods](#list_payment_methods)

 [GET 

    /v1/customers/:customer/payment_methods](#list_customer_payment_methods)

 [POST 

    /v1/payment_methods/:id/attach](#customer_attach_payment_method)

 [POST 

    /v1/payment_methods/:id/detach](#customer_detach_payment_method)

Show

Bank Accounts
=============

These bank accounts are payment methods on `Customer` objects…

Endpoints

 [POST 

    /v1/customers/:id/sources](#customer_create_bank_account)

 [GET 

    /v1/customers/:id/sources/:id](#customer_retrieve_bank_account)

 [POST 

    /v1/customers/:id/sources/:id](#customer_update_bank_account)

 [POST 

    /v1/customers/:id/sources/:id/verify](#customer_verify_bank_account)

[

    DELETE 

    /v1/customers/:id/sources/:id





](#customer_delete_bank_account)

 [GET 

    /v1/customers/:id/sources?object=bank_account](#customer_list_bank_accounts)

Show

Cards
=====

You can store multiple cards on a customer in order to charge the customer later. You can also store multiple debit cards on a recipient in order to transfer to those cards later…

Endpoints

 [POST 

    /v1/customers/:id/sources](#create_card)

 [GET 

    /v1/customers/:id/sources/:id](#retrieve_card)

 [POST 

    /v1/customers/:id/sources/:id](#update_card)

[

    DELETE 

    /v1/customers/:id/sources/:id





](#delete_card)

 [GET 

    /v1/customers/:id/sources?object=card](#list_cards)

Show

Sources
=======

`Source` objects allow you to accept a variety of payment methods. They represent a customer's payment instrument, and can be used with the Stripe API just like a `Card` object: once chargeable, they can be charged, or can be attached to customers.

Related guides: [Sources API](/docs/sources) and [Sources & Customers](/docs/sources/customers).

Was this section helpful?YesNo

Endpoints

 [POST 

    /v1/sources](#create_source)

 [GET 

    /v1/sources/:id](#retrieve_source)

 [POST 

    /v1/sources/:id](#update_source)

 [POST 

    /v1/customers/:id/sources](#attach_source)

[

    DELETE 

    /v1/customers/:id/sources/:id





](#detach_source)

The source object
=================

##### Attributes

*   ### [
    
    ](#source_object-id)id string
    
    Unique identifier for the object.
    
*   ### [
    
    ](#source_object-amount)amount integer
    
    A positive integer in the smallest currency unit (that is, 100 cents for $1.00, or 1 for ¥1, Japanese Yen being a zero-decimal currency) representing the total amount associated with the source. This is the amount for which the source will be chargeable once ready. Required for `single_use` sources.
    
*   ### [
    
    ](#source_object-currency)currency currency
    
    Three-letter [ISO code for the currency](https://stripe.com/docs/currencies) associated with the source. This is the currency for which the source will be chargeable once ready. Required for `single_use` sources.
    
*   ### [
    
    ](#source_object-customer)customer string
    
    The ID of the customer to which this source is attached. This will not be present when the source has not been attached to a customer.
    
*   ### [
    
    ](#source_object-metadata)metadata hash
    
    Set of [key-value pairs](/docs/api/metadata) that you can attach to an object. This can be useful for storing additional information about the object in a structured format.
    
*   ### [
    
    ](#source_object-owner)owner hash
    
    Information about the owner of the payment instrument that may be used or required by particular source types.
    
    ##### Show child attributes
    
*   ### [
    
    ](#source_object-redirect)redirect hash
    
    Information related to the redirect flow. Present if the source is authenticated by a redirect (`flow` is `redirect`).
    
    ##### Show child attributes
    
*   ### [
    
    ](#source_object-statement_descriptor)statement\_descriptor string
    
    Extra information about a source. This will appear on your customer’s statement every time you charge the source.
    
*   ### [
    
    ](#source_object-status)status string
    
    The status of the source, one of `canceled`, `chargeable`, `consumed`, `failed`, or `pending`. Only `chargeable` sources can be used to create a charge.
    
*   ### [
    
    ](#source_object-type)type string
    
    The `type` of the source. The `type` is a payment method, one of `ach_credit_transfer`, `ach_debit`, `alipay`, `bancontact`, `card`, `card_present`, `eps`, `giropay`, `ideal`, `multibanco`, `klarna`, `p24`, `sepa_debit`, `sofort`, `three_d_secure`, or `wechat`. An additional hash is included on the source with a name matching this value. It contains additional information specific to the [payment method](/docs/sources) used.
    

##### More attributesExpand all

*   ### [
    
    ](#source_object-object)
    
    object string, value is "source"
    
*   ### [
    
    ](#source_object-client_secret)
    
    client\_secret string
    
*   ### [
    
    ](#source_object-code_verification)
    
    code\_verification hash
    
*   ### [
    
    ](#source_object-created)
    
    created timestamp
    
*   ### [
    
    ](#source_object-flow)
    
    flow string
    
*   ### [
    
    ](#source_object-livemode)
    
    livemode boolean
    
*   ### [
    
    ](#source_object-receiver)
    
    receiver hash
    
*   ### [
    
    ](#source_object-source_order)
    
    source\_order hash
    
*   ### [
    
    ](#source_object-usage)
    
    usage string
    

The source object

    {
      "id": "src_1KIQIR2eZvKYlo2CKTQAQJkC",
      "object": "source",
      "ach_credit_transfer": {
        "account_number": "test_52796e3294dc",
        "routing_number": "110000000",
        "fingerprint": "ecpwEzmBOSMOqQTL",
        "bank_name": "TEST BANK",
        "swift_code": "TSTEZ122"
      },
      "amount": null,
      "client_secret": "src_client_secret_eAKU98qgip0tZgOvTnoRgxCy",
      "created": 1642307091,
      "currency": "usd",
      "flow": "receiver",
      "livemode": false,
      "metadata": {},
      "owner": {
        "address": null,
        "email": "jenny.rosen@example.com",
        "name": null,
        "phone": null,
        "verified_address": null,
        "verified_email": null,
        "verified_name": null,
        "verified_phone": null
      },
      "receiver": {
        "address": "121042882-38381234567890123",
        "amount_charged": 0,
        "amount_received": 0,
        "amount_returned": 0,
        "refund_attributes_method": "email",
        "refund_attributes_status": "missing"
      },
      "statement_descriptor": null,
      "status": "pending",
      "type": "ach_credit_transfer",
      "usage": "reusable"
    }

Create a source
===============

Creates a new source object.

##### Parameters

*   ### [
    
    ](#create_source-type)type required
    
    The `type` of the source to create. Required unless `customer` and `original_source` are specified (see the [Cloning card Sources](/docs/sources/connect#cloning-card-sources) guide)
    
*   ### [
    
    ](#create_source-amount)amount optional
    
    Amount associated with the source. This is the amount for which the source will be chargeable once ready. Required for `single_use` sources. Not supported for `receiver` type sources, where charge amount may not be specified until funds land.
    
*   ### [
    
    ](#create_source-currency)currency optional
    
    Three-letter [ISO code for the currency](https://stripe.com/docs/currencies) associated with the source. This is the currency for which the source will be chargeable once ready.
    
*   ### [
    
    ](#create_source-metadata)metadata optional dictionary
    
    Set of [key-value pairs](/docs/api/metadata) that you can attach to an object. This can be useful for storing additional information about the object in a structured format. Individual keys can be unset by posting an empty value to them. All keys can be unset by posting an empty value to `metadata`.
    
*   ### [
    
    ](#create_source-owner)owner optional dictionary
    
    Information about the owner of the payment instrument that may be used or required by particular source types.
    
    ##### Show child parameters
    
*   ### [
    
    ](#create_source-redirect)redirect optional dictionary
    
    Parameters required for the redirect flow. Required if the source is authenticated by a redirect (`flow` is `redirect`).
    
    ##### Show child parameters
    
*   ### [
    
    ](#create_source-statement_descriptor)statement\_descriptor optional
    
    An arbitrary string to be displayed on your customer’s statement. As an example, if your website is `RunClub` and the item you’re charging for is a race ticket, you may want to specify a `statement_descriptor` of `RunClub 5K race ticket.` While many payment types will display this information, some may not display it at all.
    

##### More parametersExpand all

*   ### [
    
    ](#create_source-flow)
    
    flow optional
    
*   ### [
    
    ](#create_source-mandate)
    
    mandate optional dictionary
    
*   ### [
    
    ](#create_source-receiver)
    
    receiver optional dictionary
    
*   ### [
    
    ](#create_source-source_order)
    
    source\_order optional dictionary
    
*   ### [
    
    ](#create_source-token)
    
    token optional
    
*   ### [
    
    ](#create_source-usage)
    
    usage optional
    

Returns
-------

Returns a newly created source.

    POST 

    /v1/sources

Select librarycURLStripe CLIRubyPythonPHPJavaNode.jsGo.NET

[

](/login?redirect=%2Ftest%2Flogs%3Fdashboard%3Dfalse%26direction%5B%5D%3Dself%26direction%5B%5D%3Dconnect_out%26method%5B%5D%3Dpost%26path%3D%252Fv1%252Fsources)

1

2

3

4

5

    curl https://api.stripe.com/v1/sources \
      -u sk_test_4eC39HqLyjWDarjtT1zdp7dc: \
      -d type=ach_credit_transfer \
      -d currency=usd \
      -d "owner[email]"="jenny.rosen@example.com"

Response

    {
      "id": "src_1KIQIR2eZvKYlo2CKTQAQJkC",
      "object": "source",
      "ach_credit_transfer": {
        "account_number": "test_52796e3294dc",
        "routing_number": "110000000",
        "fingerprint": "ecpwEzmBOSMOqQTL",
        "bank_name": "TEST BANK",
        "swift_code": "TSTEZ122"
      },
      "amount": null,
      "client_secret": "src_client_secret_eAKU98qgip0tZgOvTnoRgxCy",
      "created": 1642307091,
      "currency": "usd",
      "flow": "receiver",
      "livemode": false,
      "metadata": {},
      "owner": {
        "address": null,
        "email": "jenny.rosen@example.com",
        "name": null,
        "phone": null,
        "verified_address": null,
        "verified_email": null,
        "verified_name": null,
        "verified_phone": null
      },
      "receiver": {
        "address": "121042882-38381234567890123",
        "amount_charged": 0,
        "amount_received": 0,
        "amount_returned": 0,
        "refund_attributes_method": "email",
        "refund_attributes_status": "missing"
      },
      "statement_descriptor": null,
      "status": "pending",
      "type": "ach_credit_transfer",
      "usage": "reusable"
    }

Retrieve a source
=================

Retrieves an existing source object. Supply the unique source ID from a source creation request and Stripe will return the corresponding up-to-date source object information.

##### ParametersExpand all

*   ### [
    
    ](#retrieve_source-client_secret)
    
    client\_secret optional
    

Returns
-------

Returns a source if a valid identifier was provided.

    GET 

    /v1/sources/:id

Select librarycURLStripe CLIRubyPythonPHPJavaNode.jsGo.NET

[

](/login?redirect=%2Ftest%2Flogs%3Fdashboard%3Dfalse%26direction%5B%5D%3Dself%26direction%5B%5D%3Dconnect_out%26method%5B%5D%3Dget%26path%3D%252Fv1%252Fsources%252F%253Aid)

1

2

    curl https://api.stripe.com/v1/sources/src_1KIQIR2eZvKYlo2CKTQAQJkC \
      -u sk_test_4eC39HqLyjWDarjtT1zdp7dc:

Response

    {
      "id": "src_1KIQIR2eZvKYlo2CKTQAQJkC",
      "object": "source",
      "ach_credit_transfer": {
        "account_number": "test_52796e3294dc",
        "routing_number": "110000000",
        "fingerprint": "ecpwEzmBOSMOqQTL",
        "bank_name": "TEST BANK",
        "swift_code": "TSTEZ122"
      },
      "amount": null,
      "client_secret": "src_client_secret_eAKU98qgip0tZgOvTnoRgxCy",
      "created": 1642307091,
      "currency": "usd",
      "flow": "receiver",
      "livemode": false,
      "metadata": {},
      "owner": {
        "address": null,
        "email": "jenny.rosen@example.com",
        "name": null,
        "phone": null,
        "verified_address": null,
        "verified_email": null,
        "verified_name": null,
        "verified_phone": null
      },
      "receiver": {
        "address": "121042882-38381234567890123",
        "amount_charged": 0,
        "amount_received": 0,
        "amount_returned": 0,
        "refund_attributes_method": "email",
        "refund_attributes_status": "missing"
      },
      "statement_descriptor": null,
      "status": "pending",
      "type": "ach_credit_transfer",
      "usage": "reusable"
    }

Update a source
===============

Updates the specified source by setting the values of the parameters passed. Any parameters not provided will be left unchanged.

This request accepts the `metadata` and `owner` as arguments. It is also possible to update type specific information for selected payment methods. Please refer to our [payment method guides](/docs/sources) for more detail.

##### Parameters

*   ### [
    
    ](#update_source-amount)amount optional
    
    Amount associated with the source.
    
*   ### [
    
    ](#update_source-metadata)metadata optional dictionary
    
    Set of [key-value pairs](/docs/api/metadata) that you can attach to an object. This can be useful for storing additional information about the object in a structured format. Individual keys can be unset by posting an empty value to them. All keys can be unset by posting an empty value to `metadata`.
    
*   ### [
    
    ](#update_source-owner)owner optional dictionary
    
    Information about the owner of the payment instrument that may be used or required by particular source types.
    
    ##### Show child parameters
    

##### More parametersExpand all

*   ### [
    
    ](#update_source-mandate)
    
    mandate optional dictionary
    
*   ### [
    
    ](#update_source-source_order)
    
    source\_order optional dictionary
    

Returns
-------

Returns the source object if the update succeeded. This call will return [an error](#errors) if update parameters are invalid.

    POST 

    /v1/sources/:id

Select librarycURLStripe CLIRubyPythonPHPJavaNode.jsGo.NET

[

](/login?redirect=%2Ftest%2Flogs%3Fdashboard%3Dfalse%26direction%5B%5D%3Dself%26direction%5B%5D%3Dconnect_out%26method%5B%5D%3Dpost%26path%3D%252Fv1%252Fsources%252F%253Aid)

1

2

3

    curl https://api.stripe.com/v1/sources/src_1KIQIR2eZvKYlo2CKTQAQJkC \
      -u sk_test_4eC39HqLyjWDarjtT1zdp7dc: \
      -d "metadata[order_id]"=6735

Response

    {
      "id": "src_1KIQIR2eZvKYlo2CKTQAQJkC",
      "object": "source",
      "ach_credit_transfer": {
        "account_number": "test_52796e3294dc",
        "routing_number": "110000000",
        "fingerprint": "ecpwEzmBOSMOqQTL",
        "bank_name": "TEST BANK",
        "swift_code": "TSTEZ122"
      },
      "amount": null,
      "client_secret": "src_client_secret_eAKU98qgip0tZgOvTnoRgxCy",
      "created": 1642307091,
      "currency": "usd",
      "flow": "receiver",
      "livemode": false,
      "metadata": {
        "order_id": "6735"
      },
      "owner": {
        "address": null,
        "email": "jenny.rosen@example.com",
        "name": null,
        "phone": null,
        "verified_address": null,
        "verified_email": null,
        "verified_name": null,
        "verified_phone": null
      },
      "receiver": {
        "address": "121042882-38381234567890123",
        "amount_charged": 0,
        "amount_received": 0,
        "amount_returned": 0,
        "refund_attributes_method": "email",
        "refund_attributes_status": "missing"
      },
      "statement_descriptor": null,
      "status": "pending",
      "type": "ach_credit_transfer",
      "usage": "reusable"
    }

Attach a source
===============

Attaches a Source object to a Customer. The source must be in a chargeable or pending state.

##### Parameters

*   ### [
    
    ](#attach_source-source)source required
    
    The identifier of the source to be attached.
    

Returns
-------

Returns the attached Source object.

    POST 

    /v1/customers/:id/sources

Select librarycURLStripe CLIRubyPythonPHPJavaNode.jsGo.NET

[

](/login?redirect=%2Ftest%2Flogs%3Fdashboard%3Dfalse%26direction%5B%5D%3Dself%26direction%5B%5D%3Dconnect_out%26method%5B%5D%3Dpost%26path%3D%252Fv1%252Fcustomers%252F%253Aid%252Fsources)

1

2

3

    curl https://api.stripe.com/v1/customers/cus_AJ6yY15pe9xOZe/sources \
      -u sk_test_4eC39HqLyjWDarjtT1zdp7dc: \
      -d source=src_1KIQIR2eZvKYlo2CKTQAQJkC

Response

    {
      "id": "src_1KIQIR2eZvKYlo2CKTQAQJkC",
      "object": "source",
      "ach_credit_transfer": {
        "account_number": "test_52796e3294dc",
        "routing_number": "110000000",
        "fingerprint": "ecpwEzmBOSMOqQTL",
        "bank_name": "TEST BANK",
        "swift_code": "TSTEZ122"
      },
      "amount": 1000,
      "client_secret": "src_client_secret_eAKU98qgip0tZgOvTnoRgxCy",
      "created": 1642307091,
      "currency": "usd",
      "flow": "receiver",
      "livemode": false,
      "metadata": {},
      "owner": {
        "address": null,
        "email": "jenny.rosen@example.com",
        "name": null,
        "phone": null,
        "verified_address": null,
        "verified_email": null,
        "verified_name": null,
        "verified_phone": null
      },
      "receiver": {
        "address": "121042882-38381234567890123",
        "amount_received": 1000,
        "amount_charged": 0,
        "amount_returned": 0,
        "refund_attributes_status": "missing",
        "refund_attributes_method": "email"
      },
      "statement_descriptor": null,
      "status": "chargeable",
      "type": "ach_credit_transfer",
      "usage": "reusable",
      "customer": "cus_AJ6yY15pe9xOZe"
    }

Detach a source
===============

Detaches a Source object from a Customer. The status of a source is changed to `consumed` when it is detached and it can no longer be used to create a charge.

##### Parameters

*   ### No parameters.
    

Returns
-------

Returns the detached Source object.

    DELETE 

    /v1/customers/:id/sources/:id

Select librarycURLStripe CLIRubyPythonPHPJavaNode.jsGo.NET

[

](/login?redirect=%2Ftest%2Flogs%3Fdashboard%3Dfalse%26direction%5B%5D%3Dself%26direction%5B%5D%3Dconnect_out%26method%5B%5D%3Ddelete%26path%3D%252Fv1%252Fcustomers%252F%253Aid%252Fsources%252F%253Aid)

1

2

3

    curl https://api.stripe.com/v1/customers/cus_AJ6yY15pe9xOZe/sources/src_1KIQIR2eZvKYlo2CKTQAQJkC \
      -u sk_test_4eC39HqLyjWDarjtT1zdp7dc: \
      -X DELETE

Response

    {
      "id": "src_1KIQIR2eZvKYlo2CKTQAQJkC",
      "object": "source",
      "ach_credit_transfer": {
        "account_number": "test_52796e3294dc",
        "routing_number": "110000000",
        "fingerprint": "ecpwEzmBOSMOqQTL",
        "bank_name": "TEST BANK",
        "swift_code": "TSTEZ122"
      },
      "amount": 0,
      "client_secret": "src_client_secret_eAKU98qgip0tZgOvTnoRgxCy",
      "created": 1642307091,
      "currency": "usd",
      "flow": "receiver",
      "livemode": false,
      "metadata": {},
      "owner": {
        "address": null,
        "email": "jenny.rosen@example.com",
        "name": null,
        "phone": null,
        "verified_address": null,
        "verified_email": null,
        "verified_name": null,
        "verified_phone": null
      },
      "receiver": {
        "address": "121042882-38381234567890123",
        "amount_received": 1000,
        "amount_charged": 1000,
        "amount_returned": 0,
        "refund_attributes_status": "missing",
        "refund_attributes_method": "email"
      },
      "statement_descriptor": null,
      "status": "consumed",
      "type": "ach_credit_transfer",
      "usage": "reusable",
      "customer": "cus_AJ6yY15pe9xOZe"
    }

Products
========

Products describe the specific goods or services you offer to your customers. For example, you might offer a Standard and Premium version of your goods or service; each version would be a separate Product. They can be used in conjunction with [Prices](#prices) to configure pricing in Checkout and Subscriptions…

Endpoints

 [POST 

    /v1/products](#create_product)

 [GET 

    /v1/products/:id](#retrieve_product)

 [POST 

    /v1/products/:id](#update_product)

 [GET 

    /v1/products](#list_products)

[

    DELETE 

    /v1/products/:id





](#delete_product)

Show

Prices
======

Prices define the unit cost, currency, and (optional) billing cycle for both recurring and one-time purchases of products. [Products](#products) help you track inventory or provisioning, and prices help you track payment terms. Different physical goods or levels of service should be represented by products, and pricing options should be represented by prices. This approach lets you change prices without having to change your provisioning scheme…

Endpoints

 [POST 

    /v1/prices](#create_price)

 [GET 

    /v1/prices/:id](#retrieve_price)

 [POST 

    /v1/prices/:id](#update_price)

 [GET 

    /v1/prices](#list_prices)

Show

Coupons
=======

A coupon contains information about a percent-off or amount-off discount you might want to apply to a customer. Coupons may be applied to [invoices](#invoices) or [orders](#create_order_legacy-coupon). Coupons do not work with conventional one-off [charges](#create_charge).

Endpoints

 [POST 

    /v1/coupons](#create_coupon)

 [GET 

    /v1/coupons/:id](#retrieve_coupon)

 [POST 

    /v1/coupons/:id](#update_coupon)

[

    DELETE 

    /v1/coupons/:id





](#delete_coupon)

 [GET 

    /v1/coupons](#list_coupons)

Show

Promotion Code
==============

A Promotion Code represents a customer-redeemable code for a coupon. It can be used to create multiple codes for a single coupon.

Endpoints

 [POST 

    /v1/promotion_codes](#create_promotion_code)

 [POST 

    /v1/promotion_codes/:id](#update_promotion_code)

 [GET 

    /v1/promotion_codes/:id](#retrieve_promotion_code)

 [GET 

    /v1/promotion_codes](#list_promotion_code)

Show

Discounts
=========

A discount represents the actual application of a coupon to a particular customer. It contains information about when the discount began and when it will end…

Endpoints

[

    DELETE 

    /v1/customers/:id/discount





](#delete_discount)

[

    DELETE 

    /v1/subscriptions/:id/discount





](#delete_subscription_discount)

Show

Tax Code
========

[Tax codes](https://stripe.com/docs/tax/tax-codes) classify goods and services for tax purposes.

Endpoints

 [GET 

    /v1/tax_codes](#list_tax_codes)

 [GET 

    /v1/tax_codes/:id](#retrieve_taxcode)

Show

Tax Rate
========

Tax rates can be applied to [invoices](/docs/billing/invoices/tax-rates), [subscriptions](/docs/billing/subscriptions/taxes) and [Checkout Sessions](/docs/payments/checkout/set-up-a-subscription#tax-rates) to collect tax…

Endpoints

 [POST 

    /v1/tax_rates](#create_tax_rate)

 [GET 

    /v1/tax_rates/:id](#retrieve_tax_rate)

 [POST 

    /v1/tax_rates/:id](#update_tax_rate)

 [GET 

    /v1/tax_rates](#list_tax_rates)

Show

Shipping Rates
==============

Shipping rates describe the price of shipping presented to your customers and can be applied to [Checkout Sessions](/docs/payments/checkout/shipping) to collect shipping costs.

Endpoints

 [POST 

    /v1/shipping_rates](#create_shipping_rate)

 [GET 

    /v1/shipping_rates/:id](#retrieve_shipping_rate)

 [POST 

    /v1/shipping_rates/:id](#update_shipping_rate)

 [GET 

    /v1/shipping_rates](#list_shipping_rates)

Show

Sessions
========

A Checkout Session represents your customer's session as they pay for one-time purchases or subscriptions through [Checkout](/docs/payments/checkout) or [Payment Links](/docs/payments/payment-links). We recommend creating a new Session each time your customer attempts to pay…

Endpoints

 [POST 

    /v1/checkout/sessions](#create_checkout_session)

 [POST 

    /v1/checkout/sessions/:id/expire](#expire_checkout_session)

 [GET 

    /v1/checkout/sessions/:id](#retrieve_checkout_session)

 [GET 

    /v1/checkout/sessions](#list_checkout_sessions)

 [GET 

    /v1/checkout/sessions/:id/line_items](#retrieve_checkout_session_line_items)

Show

Credit Note
===========

Issue a credit note to adjust an invoice's amount after the invoice is finalized…

Endpoints

 [GET 

    /v1/credit_notes/preview](#preview_credit_note)

 [POST 

    /v1/credit_notes](#create_credit_note)

 [GET 

    /v1/credit_notes/:id](#retrieve_credit_note)

 [POST 

    /v1/credit_notes/:id](#update_credit_note)

 [GET 

    /v1/credit_notes/:credit_note/lines](#credit_note_lines)

 [GET 

    /v1/credit_notes/preview/lines](#credit_note_preview_lines)

 [POST 

    /v1/credit_notes/:id/void](#void_credit_note)

 [GET 

    /v1/credit_notes](#list_credit_notes)

Show

Customer Balance Transaction
============================

Each customer has a [`balance`](/docs/api/customers/object#customer_object-balance) value, which denotes a debit or credit that's automatically applied to their next invoice upon finalization. You may modify the value directly by using the [update customer API](#update_customer), or by creating a Customer Balance Transaction, which increments or decrements the customer's `balance` by the specified `amount`…

Endpoints

 [POST 

    /v1/customers/:id/balance_transactions](#create_customer_balance_transaction)

 [GET 

    /v1/customers/:id/balance_transactions/:id](#retrieve_customer_balance_transaction)

 [POST 

    /v1/customers/:id/balance_transactions/:id](#update_customer_balance_transaction)

 [GET 

    /v1/customers/:id/balance_transactions](#list_customer_balance_transactions)

Show

Customer Portal
===============

The Billing customer portal is a Stripe-hosted UI for subscription and billing management…

Endpoints

 [POST 

    /v1/billing_portal/sessions](#create_portal_session)

 [POST 

    /v1/billing_portal/configurations](#create_portal_configuration)

 [POST 

    /v1/billing_portal/configurations/:id](#update_portal_configuration)

 [GET 

    /v1/billing_portal/configurations/:id](#retrieve_portal_configuration)

 [GET 

    /v1/billing_portal/configurations](#all_portal_configurations)

Show

Customer Tax IDs
================

You can add one or multiple tax IDs to a [customer](#customers). A customer's tax IDs are displayed on invoices and credit notes issued for the customer…

Endpoints

 [POST 

    /v1/customers/:id/tax_ids](#create_tax_id)

 [GET 

    /v1/customers/:id/tax_ids/:id](#retrieve_tax_id)

[

    DELETE 

    /v1/customers/:id/tax_ids/:id





](#delete_tax_id)

 [GET 

    /v1/customers/:id/tax_ids](#list_tax_ids)

Show

Invoices
========

Invoices are statements of amounts owed by a customer, and are either generated one-off, or generated periodically from a subscription…

Endpoints

 [POST 

    /v1/invoices](#create_invoice)

 [GET 

    /v1/invoices/:id](#retrieve_invoice)

 [POST 

    /v1/invoices/:id](#update_invoice)

[

    DELETE 

    /v1/invoices/:id





](#delete_invoice)

 [POST 

    /v1/invoices/:id/finalize](#finalize_invoice)

 [POST 

    /v1/invoices/:id/pay](#pay_invoice)

 [POST 

    /v1/invoices/:id/send](#send_invoice)

 [POST 

    /v1/invoices/:id/void](#void_invoice)

 [POST 

    /v1/invoices/:id/mark_uncollectible](#mark_uncollectible_invoice)

 [GET 

    /v1/invoices/:id/lines](#invoice_lines)

 [GET 

    /v1/invoices/upcoming](#upcoming_invoice)

 [GET 

    /v1/invoices/upcoming/lines](#upcoming_invoice_lines)

 [GET 

    /v1/invoices](#list_invoices)

Show

Invoice Items
=============

Sometimes you want to add a charge or credit to a customer, but actually charge or credit the customer's card only at the end of a regular billing cycle. This is useful for combining several charges (to minimize per-transaction fees), or for having Stripe tabulate your usage-based billing totals…

Endpoints

 [POST 

    /v1/invoiceitems](#create_invoiceitem)

 [GET 

    /v1/invoiceitems/:id](#retrieve_invoiceitem)

 [POST 

    /v1/invoiceitems/:id](#update_invoiceitem)

[

    DELETE 

    /v1/invoiceitems/:id





](#delete_invoiceitem)

 [GET 

    /v1/invoiceitems](#list_invoiceitems)

Show

Plans
=====

You can now model subscriptions more flexibly using the [Prices API](#prices). It replaces the Plans API and is backwards compatible to simplify your migration…

Endpoints

 [POST 

    /v1/plans](#create_plan)

 [GET 

    /v1/plans/:id](#retrieve_plan)

 [POST 

    /v1/plans/:id](#update_plan)

[

    DELETE 

    /v1/plans/:id





](#delete_plan)

 [GET 

    /v1/plans](#list_plans)

Show

Quote
=====

A Quote is a way to model prices that you'd like to provide to a customer. Once accepted, it will automatically create an invoice, subscription or subscription schedule.

Endpoints

 [POST 

    /v1/quotes](#create_quote)

 [GET 

    /v1/quotes/:id](#retrieve_quote)

 [POST 

    /v1/quotes/:id](#update_quote)

 [POST 

    /v1/quotes/:id/finalize](#finalize_quote)

 [POST 

    /v1/quotes/:id/accept](#accept_quote)

 [POST 

    /v1/quotes/:id/cancel](#cancel_quote)

 [GET 

    https://files.stripe.com/v1/quotes/:id/pdf](#download_pdf_method)

 [GET 

    /v1/quotes](#list_quote)

 [GET 

    /v1/quotes/:id/line_items](#list_line_item)

 [GET 

    /v1/quotes/:id/computed_upfront_line_items](#list_upfront_line_item)

Show

Subscriptions
=============

Subscriptions allow you to charge a customer on a recurring basis…

Endpoints

 [POST 

    /v1/subscriptions](#create_subscription)

 [GET 

    /v1/subscriptions/:id](#retrieve_subscription)

 [POST 

    /v1/subscriptions/:id](#update_subscription)

[

    DELETE 

    /v1/subscriptions/:id





](#cancel_subscription)

 [GET 

    /v1/subscriptions](#list_subscriptions)

Show

Subscription Items
==================

Subscription items allow you to create customer subscriptions with more than one plan, making it easy to represent complex billing relationships.

Endpoints

 [POST 

    /v1/subscription_items](#create_subscription_item)

 [GET 

    /v1/subscription_items/:id](#retrieve_subscription_item)

 [POST 

    /v1/subscription_items/:id](#update_subscription_item)

[

    DELETE 

    /v1/subscription_items/:id





](#delete_subscription_item)

 [GET 

    /v1/subscription_items](#list_subscription_items)

Show

Subscription Schedule
=====================

A subscription schedule allows you to create and manage the lifecycle of a subscription by predefining expected changes…

Endpoints

 [POST 

    /v1/subscription_schedules](#create_subscription_schedule)

 [GET 

    /v1/subscription_schedules/:id](#retrieve_subscription_schedule)

 [POST 

    /v1/subscription_schedules/:id](#update_subscription_schedule)

 [POST 

    /v1/subscription_schedules/:id/cancel](#cancel_subscription_schedule)

 [POST 

    /v1/subscription_schedules/:id/release](#release_subscription_schedule)

 [GET 

    /v1/subscription_schedules](#list_subscription_schedules)

Show

Usage Records
=============

Usage records allow you to report customer usage and metrics to Stripe for metered billing of subscription prices…

Endpoints

 [POST 

    /v1/subscription_items/:id/usage_records](#usage_record_create)

 [GET 

    /v1/subscription_items/:id/usage_record_summaries](#usage_record_summary_all)

Show

Accounts
========

This is an object representing a Stripe account. You can retrieve it to see properties on the account like its current e-mail address or if the account is enabled yet to make live charges…

Endpoints

 [POST 

    /v1/accounts](#create_account)

 [GET 

    /v1/accounts/:id](#retrieve_account)

 [POST 

    /v1/accounts/:id](#update_account)

[

    DELETE 

    /v1/accounts/:id





](#delete_account)

 [POST 

    /v1/accounts/:id/reject](#reject_account)

 [GET 

    /v1/accounts](#list_accounts)

 [POST 

    /v1/login_links](#create_login_link)

Show

Account Links
=============

Account Links are the means by which a Connect platform grants a connected account permission to access Stripe-hosted applications, such as Connect Onboarding…

Endpoints

 [POST 

    /v1/account_links](#create_account_link)

Show

Application Fees
================

When you collect a transaction fee on top of a charge made for your user (using [Connect](/docs/connect)), an `Application Fee` object is created in your account. You can list, retrieve, and refund application fees…

Endpoints

 [GET 

    /v1/application_fees/:id](#retrieve_application_fee)

 [GET 

    /v1/application_fees](#list_application_fees)

Show

Application Fee Refunds
=======================

`Application Fee Refund` objects allow you to refund an application fee that has previously been created but not yet refunded. Funds will be refunded to the Stripe account from which the fee was originally collected…

Endpoints

 [POST 

    /v1/application_fees/:id/refunds](#create_fee_refund)

 [GET 

    /v1/application_fees/:id/refunds/:id](#retrieve_fee_refund)

 [POST 

    /v1/application_fees/:id/refunds/:id](#update_fee_refund)

 [GET 

    /v1/application_fees/:id/refunds](#list_fee_refunds)

Show

Capabilities
============

This is an object representing a capability for a Stripe account…

Endpoints

 [GET 

    /v1/accounts/:id/capabilities/:id](#retrieve_capability)

 [POST 

    /v1/accounts/:id/capabilities/:id](#update_capability)

 [GET 

    /v1/accounts/:id/capabilities](#list_capability)

Show

Country Specs
=============

Stripe needs to collect certain pieces of information about each account created. These requirements can differ depending on the account's country. The Country Specs API makes these rules available to your integration…

Endpoints

 [GET 

    /v1/country_specs](#list_country_specs)

 [GET 

    /v1/country_specs/:id](#retrieve_country_spec)

Show

External Accounts
=================

External Accounts are transfer destinations on `Account` objects for [connected accounts](/docs/connect/accounts). They can be bank accounts or debit cards…

Endpoints

 [POST 

    /v1/accounts/:id/external_accounts](#account_create_bank_account)

 [GET 

    /v1/accounts/:id/external_accounts/:id](#account_retrieve_bank_account)

 [POST 

    /v1/accounts/:id/external_accounts/:id](#account_update_bank_account)

[

    DELETE 

    /v1/accounts/:id/external_accounts/:id





](#account_delete_bank_account)

 [GET 

    /v1/accounts/:id/external_accounts?object=bank_account](#account_list_bank_accounts)

 [POST 

    /v1/accounts/:id/external_accounts](#account_create_card)

 [GET 

    /v1/accounts/:id/external_accounts/:id](#account_retrieve_card)

 [POST 

    /v1/accounts/:id/external_accounts/:id](#account_update_card)

[

    DELETE 

    /v1/accounts/:id/external_accounts/:id





](#account_delete_card)

 [GET 

    /v1/accounts/:id/external_accounts?object=card](#account_list_cards)

Show

Person
======

This is an object representing a person associated with a Stripe account…

Endpoints

 [POST 

    /v1/accounts/:id/persons](#create_person)

 [GET 

    /v1/accounts/:id/persons/:id](#retrieve_person)

 [POST 

    /v1/accounts/:id/persons/:id](#update_person)

[

    DELETE 

    /v1/accounts/:id/persons/:id





](#delete_person)

 [GET 

    /v1/accounts/:id/persons](#list_person)

Show

Top-ups
=======

To top up your Stripe balance, you create a top-up object. You can retrieve individual top-ups, as well as list all top-ups. Top-ups are identified by a unique, random ID…

Endpoints

 [POST 

    /v1/topups](#create_topup)

 [GET 

    /v1/topups/:id](#retrieve_topup)

 [POST 

    /v1/topups/:id](#update_topup)

 [GET 

    /v1/topups](#list_topups)

 [POST 

    /v1/topups/:id/cancel](#cancel_topup)

Show

Transfers
=========

A `Transfer` object is created when you move funds between Stripe accounts as part of Connect…

Endpoints

 [POST 

    /v1/transfers](#create_transfer)

 [GET 

    /v1/transfers/:id](#retrieve_transfer)

 [POST 

    /v1/transfers/:id](#update_transfer)

 [GET 

    /v1/transfers](#list_transfers)

Show

Transfer Reversals
==================

[Stripe Connect](/docs/connect) platforms can reverse transfers made to a connected account, either entirely or partially, and can also specify whether to refund any related application fees. Transfer reversals add to the platform's balance and subtract from the destination account's balance…

Endpoints

 [POST 

    /v1/transfers/:id/reversals](#create_transfer_reversal)

 [GET 

    /v1/transfers/:id/reversals/:id](#retrieve_transfer_reversal)

 [POST 

    /v1/transfers/:id/reversals/:id](#update_transfer_reversal)

 [GET 

    /v1/transfers/:id/reversals](#list_transfer_reversals)

Show

Early Fraud Warning
===================

An early fraud warning indicates that the card issuer has notified us that a charge may be fraudulent…

Endpoints

 [GET 

    /v1/radar/early_fraud_warnings/:id](#retrieve_early_fraud_warning)

 [GET 

    /v1/radar/early_fraud_warnings](#list_early_fraud_warnings)

Show

Reviews
=======

Reviews can be used to supplement automated fraud detection with human expertise…

Endpoints

 [POST 

    /v1/reviews/:id/approve](#approve_review)

 [GET 

    /v1/reviews/:id](#retrieve_review)

 [GET 

    /v1/reviews](#list_reviews)

Show

Value Lists
===========

Value lists allow you to group values together which can then be referenced in rules…

Endpoints

 [POST 

    /v1/radar/value_lists](#create_value_list)

 [GET 

    /v1/radar/value_lists/:id](#retrieve_value_list)

 [POST 

    /v1/radar/value_lists/:id](#update_value_list)

[

    DELETE 

    /v1/radar/value_lists/:id





](#delete_value_list)

 [GET 

    /v1/radar/value_lists](#list_value_lists)

Show

Value List Items
================

Value list items allow you to add specific values to a given Radar value list, which can then be used in rules…

Endpoints

 [POST 

    /v1/radar/value_list_items](#create_value_list_item)

 [GET 

    /v1/radar/value_list_items/:id](#retrieve_value_list_item)

[

    DELETE 

    /v1/radar/value_list_items/:id





](#delete_value_list_item)

 [GET 

    /v1/radar/value_list_items](#list_value_list_items)

Show

Authorizations
==============

When an [issued card](/docs/issuing) is used to make a purchase, an Issuing `Authorization` object is created. [Authorizations](/docs/issuing/purchases/authorizations) must be approved for the purchase to be completed successfully…

Endpoints

 [GET 

    /v1/issuing/authorizations/:id](#retrieve_issuing_authorization)

 [POST 

    /v1/issuing/authorizations/:id](#update_issuing_authorization)

 [POST 

    /v1/issuing/authorizations/:id/approve](#approve_issuing_authorization)

 [POST 

    /v1/issuing/authorizations/:id/decline](#decline_issuing_authorization)

 [GET 

    /v1/issuing/authorizations](#list_issuing_authorizations)

Show

Cardholders
===========

An Issuing `Cardholder` object represents an individual or business entity who is [issued](/docs/issuing) cards…

Endpoints

 [POST 

    /v1/issuing/cardholders](#create_issuing_cardholder)

 [GET 

    /v1/issuing/cardholders/:id](#retrieve_issuing_cardholder)

 [POST 

    /v1/issuing/cardholders/:id](#update_issuing_cardholder)

 [GET 

    /v1/issuing/cardholders](#list_issuing_cardholders)

Show

Cards
=====

You can [create physical or virtual cards](/docs/issuing/cards) that are issued to cardholders.

Endpoints

 [POST 

    /v1/issuing/cards](#create_issuing_card)

 [GET 

    /v1/issuing/cards/:id](#retrieve_issuing_card)

 [POST 

    /v1/issuing/cards/:id](#update_issuing_card)

 [GET 

    /v1/issuing/cards](#list_issuing_cards)

Show

Disputes
========

As a [card issuer](/docs/issuing), you can dispute transactions that the cardholder does not recognize, suspects to be fraudulent, or has other issues with…

Endpoints

 [POST 

    /v1/issuing/disputes](#create_issuing_dispute)

 [POST 

    /v1/issuing/disputes/:id/submit](#submit_issuing_dispute)

 [GET 

    /v1/issuing/disputes/:id](#retrieve_issuing_dispute)

 [POST 

    /v1/issuing/disputes/:id](#update_issuing_dispute)

 [GET 

    /v1/issuing/disputes](#list_issuing_disputes)

Show

Transactions
============

Any use of an [issued card](/docs/issuing) that results in funds entering or leaving your Stripe account, such as a completed purchase or refund, is represented by an Issuing `Transaction` object…

Endpoints

 [GET 

    /v1/issuing/transactions/:id](#retrieve_issuing_transaction)

 [POST 

    /v1/issuing/transactions/:id](#update_issuing_transaction)

 [GET 

    /v1/issuing/transactions](#list_issuing_transactions)

Show

Connection Token
================

A Connection Token is used by the Stripe Terminal SDK to connect to a reader…

Endpoints

 [POST 

    /v1/terminal/connection_tokens](#create_terminal_connection_token)

Show

Location
========

A Location represents a grouping of readers…

Endpoints

 [POST 

    /v1/terminal/locations](#create_terminal_location)

 [GET 

    /v1/terminal/locations/:id](#retrieve_terminal_location)

 [POST 

    /v1/terminal/locations/:id](#update_terminal_location)

[

    DELETE 

    /v1/terminal/locations/:id





](#delete_terminal_location)

 [GET 

    /v1/terminal/locations](#list_terminal_locations)

Show

Reader
======

A Reader represents a physical device for accepting payment details…

Endpoints

 [POST 

    /v1/terminal/readers](#create_terminal_reader)

 [GET 

    /v1/terminal/readers/:id](#retrieve_terminal_reader)

 [POST 

    /v1/terminal/readers/:id](#update_terminal_reader)

[

    DELETE 

    /v1/terminal/readers/:id





](#delete_terminal_reader)

 [GET 

    /v1/terminal/readers](#list_terminal_reader)

Show

Orders
======

Order objects are created to handle end customers' purchases of previously defined [products](#products). You can create, retrieve, and pay individual orders, as well as list all orders. Orders are identified by a unique, random ID…

Endpoints

 [POST 

    /v1/orders](#create_order_legacy)

 [GET 

    /v1/orders/:id](#retrieve_order_legacy)

 [POST 

    /v1/orders/:id](#update_order_legacy)

 [POST 

    /v1/orders/:id/pay](#pay_order_legacy)

 [GET 

    /v1/orders](#list_orders_legacy)

 [POST 

    /v1/orders/:id/returns](#return_order_legacy)

Show

Order Items
===========

A representation of the constituent items of any given order. Can be used to represent [SKUs](#skus), shipping costs, or taxes owed on the order…

Show

Returns
=======

A return represents the full or partial return of a number of [order items](#order_items). Returns always belong to an order, and may optionally contain a refund…

Endpoints

 [GET 

    /v1/order_returns/:id](#retrieve_order_return)

 [GET 

    /v1/order_returns](#list_order_returns)

Show

SKUs
====

Stores representations of [stock keeping units](http://en.wikipedia.org/wiki/Stock_keeping_unit). SKUs describe specific product variations, taking into account any combination of: attributes, currency, and cost. For example, a product may be a T-shirt, whereas a specific SKU represents the `size: large`, `color: red` version of that shirt…

Endpoints

 [POST 

    /v1/skus](#create_sku)

 [GET 

    /v1/skus/:id](#retrieve_sku)

 [POST 

    /v1/skus/:id](#update_sku)

 [GET 

    /v1/skus](#list_skus)

[

    DELETE 

    /v1/skus/:id





](#delete_sku)

Show

Scheduled Queries
=================

If you have [scheduled a Sigma query](/docs/sigma/scheduled-queries), you'll receive a `sigma.scheduled_query_run.created` webhook each time the query runs. The webhook contains a `ScheduledQueryRun` object, which you can use to retrieve the query results.

Endpoints

 [GET 

    /v1/sigma/scheduled_query_runs/:id](#retrieve_scheduled_query_run)

 [GET 

    /v1/sigma/scheduled_query_runs](#list_scheduled_query_run)

Show

Report Runs
===========

The Report Run object represents an instance of a report type generated with specific run parameters. Once the object is created, Stripe begins processing the report. When the report has finished running, it will give you a reference to a file where you can retrieve your results. For an overview, see [API Access to Reports](/docs/reporting/statements/api)…

Endpoints

 [POST 

    /v1/reporting/report_runs](#create_reporting_report_run)

 [GET 

    /v1/reporting/report_runs/:id](#retrieve_reporting_report_run)

 [GET 

    /v1/reporting/report_runs](#list_reporting_report_run)

Show

Report Types
============

The Report Type resource corresponds to a particular type of report, such as the "Activity summary" or "Itemized payouts" reports. These objects are identified by an ID belonging to a set of enumerated values. See [API Access to Reports documentation](/docs/reporting/statements/api) for those Report Type IDs, along with required and optional parameters…

Endpoints

 [GET 

    /v1/reporting/report_types/:id](#retrieve_reporting_report_type)

 [GET 

    /v1/reporting/report_types](#list_reporting_report_type)

Show

VerificationSession
===================

A VerificationSession guides you through the process of collecting and verifying the identities of your users. It contains details about the type of verification, such as what [verification check](/docs/identity/verification-checks) to perform. Only create one VerificationSession for each verification in your system…

Endpoints

 [POST 

    /v1/identity/verification_sessions](#create_identity_verification_session)

 [GET 

    /v1/identity/verification_sessions](#list_identity_verification_session)

 [GET 

    /v1/identity/verification_sessions/:id](#retrieve_identity_verification_session)

 [POST 

    /v1/identity/verification_sessions/:id](#update_identity_verification_session)

 [POST 

    /v1/identity/verification_sessions/:id/cancel](#cancel_identity_verification_session)

 [POST 

    /v1/identity/verification_sessions/:id/redact](#redact_identity_verification_session)

Show

VerificationReport
==================

A VerificationReport is the result of an attempt to collect and verify data from a user. The collection of verification checks performed is determined from the `type` and `options` parameters used. You can find the result of each verification check performed in the appropriate sub-resource: `document`, `id_number`, `selfie`…

Endpoints

 [GET 

    /v1/identity/verification_reports/:id](#retrieve_identity_verification_report)

 [GET 

    /v1/identity/verification_reports](#list_identity_verification_report)

Show

Webhook Endpoints
=================

You can configure [webhook endpoints](/docs/webhooks/) via the API to be notified about events that happen in your Stripe account or connected accounts…

Endpoints

 [POST 

    /v1/webhook_endpoints](#create_webhook_endpoint)

 [GET 

    /v1/webhook_endpoints/:id](#retrieve_webhook_endpoint)

 [POST 

    /v1/webhook_endpoints/:id](#update_webhook_endpoint)

 [GET 

    /v1/webhook_endpoints](#list_webhook_endpoints)

[

    DELETE 

    /v1/webhook_endpoints/:id





](#delete_webhook_endpoints)

Show