---
title: Login Form
overview: 'Generate a `<form>` tag to authenticate a user.'
parameters:
  -
    name: redirect
    type: string
    description: >
      Where the user should be taken after
      successfully logging in.
variables:
  -
    name: errors
    type: array
    description: An array of validation errors.
id: 7432f1cb-7418-4d54-8e65-51b1ae3bcb3a
---
## Example {#example}

A basic login form, with validation errors.

```
{{ user:login_form }}

    {{ if errors }}
        <div class="alert alert-danger">
            {{ errors }}
                {{ value }}<br>
            {{ /errors }}
        </div>
    {{ /if }}


    <label>Username</label>
    <input type="text" name="username" value="{{ old:username }}" />

    <label>Password</label>
    <input type="password" name="password" value="{{ old:password }}" />

    <button>Log in</button>

{{ /user:login_form }}
```
