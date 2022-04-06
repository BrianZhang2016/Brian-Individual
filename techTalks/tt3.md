{% include navigation.html %}

# Week 4: TT3

# Tech Talks

{% include tt.html %}

## Accounts and Login

Inheritance: Getting information from another developer and adding it to the class. (OOP)

Authenticated: Approved to login

````
@login_manager.unauthorized_handler
def unauthorized():
    """Redirect unauthorized users to Login page."""
    return redirect(url_for('crud.crud_login'))
````
-Returns User to login page if they didn't log in.
