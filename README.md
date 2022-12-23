

## Steps 
- install laravel breeze + testing it.
- change users model by your custom model in config/auth.php file.
- change User Model to your custom model wherever it's necessary in the controllers & custom requests.
- testing.
- change 'web' guard to your custom guard.
- change middleware 'auth'/'guest' to auth:your-guard/guest:your-guard wherever it's necessary.
- change Auth::login , Auth::logout, Auth::___ to Auth::guard('custom_guard')->login() .... wherever it's necessary.
- testing (confirm that your guard is not a default in the config/auth.php one before testing).
- Reset password change Password::sendRestLink to Password::broker()->sendresetlink() in PasswordResetLink.
- testing (confirm that there isn't any default password in config/auth.php before tesing).

## Usefull links: 
* [https://github.com/codewithdary/laravel-breeze] : verifying email addresses before registering or updating.
* [https://stackoverflow.com/questions/36354758/laravel-password-resets-for-multiple-auth]
