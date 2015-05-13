# Errors

The Firstcar API uses the following error codes:

Error Code | Meaning
---------- | -------
401 | unauthorized -- Wrong api key or authentication token or password
404 | not_found -- The specified resource could not be found
500 | internal_server_error -- Unexpected condition was encountered
600 | missing_parameter -- Missing required parameter
601 | create_failed -- Can not create resource
602 | update_failed -- Can not update the specified resource
