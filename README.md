emailroleassign
===============

Lightweight drupal module that allows administrators to set up automated role assignment depending on the user's email domain name.

For Drupal 7.x, place the emailroleassign folder in `[drupalinstallation]/sites/all/modules/` and enable the module from the Drupal administrator module configuration page.

The configuration page can then be found at `[drupalurl]/admin/config/emailroleassign`.


custom_hook.php
===============
Custom hook for the simplesaml authentication module for Moodle.  Allows the synchronization of drupal roles that have the same Moodle role short name.  Upon account creation, the saml roles are checked to see if any equivalent short names exist as a moodle role, if so they are assigned to the new user.  The permissions of this role have to be set in Moodle's configuration, as the custom hook is only responsible for assigning the role, not for any role permissions.  This file replaces the custom_hook.php file in `[moodle_installation]/auth/saml/custom_hook.php`.
