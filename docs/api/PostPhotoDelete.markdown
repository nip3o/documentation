Delete Photo
=======================


----------------------------------------

1. [Purpose][purpose]
1. [Endpoint][endpoint]
1. [Parameters][parameters]
1. [Examples][examples]
  * [Command line][example-cli]
  * [PHP][example-php]
  * [Python][example-python]
1. [Response][response]
  * [Sample][sample]

----------------------------------------

<a name="purpose"></a>
### Purpose of the delete action API

Use this API to delete an action.

----------------------------------------

<a name="endpoint"></a>
### Endpoint

_Authentication: required_

    POST /photo/:id/delete.json

<a name="parameters"></a>
### Parameters

_None_

----------------------------------------

<a name="examples"></a>
### Examples

<a name="example-cli"></a>
#### Command Line (using [openphoto-php][openphoto-php])

    ./openphoto -p -X POST -h current.openphoto.me -e /photo/a/delete.json

<a name="example-php"></a>
#### PHP (using [openphoto-php][openphoto-php])

    $client = new OpenPhotoOAuth($host, $consumerKey, $consumerSecret, $oauthToken, $oauthTokenSecret);
    $response = $client->post("/photo/a/delete.json");

<a name="example-python"></a>
#### Python (using [openphoto-python][openphoto-python])

    client = openphoto.OpenPhoto()
    photo = client.photos.list()[0] # Returns the first photo in the list
    photo.delete()

----------------------------------------

<a name="response"></a>
### Response

The response is in a standard [response envelope](http://theopenphotoproject.org/documentation/api/Envelope).

* _message_, A string describing the result. Don't use this for anything but reading.
* _code_, _204_ on success
* _result_, Boolean

<a name="sample"></a>
#### Sample

    {
      "message":"",
      "code":204,
      "result":true
    }


[purpose]: #purpose
[endpoint]: #endpoint
[parameters]: #parameters
[examples]: #examples
[example-cli]: #example-cli
[example-php]: #example-php
[example-python]: #example-python
[response]: #response
[sample]: #sample
[openphoto-php]: https://github.com/photo/openphoto-php
[openphoto-python]: https://github.com/photo/openphoto-python
