# Errors

The Firstcar API uses the following error codes:

Error Code | Meaning
---------- | -------
600 | unknown -- server unknown error
601 | record_not_found -- The specified user could not be found
602 | authenticate_failed -- The api key is wrong
603 | wrong_authentication_token -- The authentication token is wrong
604 | user_create_failed -- Can not create user
605 | session_create_failed -- Can not sign user in
606 | password_create_failed -- Can not create reset password token
607 | wrong_reset_password_token -- Wrong reset password token
608 | password_update_failed -- Can not update password
609 | invalid_password -- Invalid or missing new password
610 | missing_checklist_id -- Missing checklist id
611 | user_update_failed -- Can not update user
612 | missing_postcode -- Missing postcode
