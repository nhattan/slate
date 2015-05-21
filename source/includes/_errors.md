# Errors

The Firstcar API uses the following error codes:

Error Code | Meaning
---------- | -------
400 | bad_request -- Missing or invalid parameter
401 | unauthorized -- Wrong api key or authentication token or password
404 | not_found -- The specified resource could not be found
500 | internal_server_error -- Unexpected condition was encountered
600 | create_failed -- Can not create resource
601 | update_failed -- Can not update the specified resource
602 | task_not_found -- Can not found the task
603 | checklist_not_found -- Can not found the checklist
