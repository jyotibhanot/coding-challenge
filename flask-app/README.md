#flask-app

Ansible role for provisioning and deploying Flask application.

## Features

  * Provides tasks for provisioning and deploying a Flask application.
  * Provisions a server with all required applications and requirements.
  * Easily deploy your Flask application
  * Use git to checkout the application
  * Use Nginx as reverse proxy
  * Use Supervisor as process manager
  * Enable and start services

###Dependencies

None 

#### Add the role to your playbook

Add the *flask-app* role to your *playbook*:

```yaml
- hosts: all
  roles:
    - {role: flask-app,
       tags: [flaskapp]}
```

This executes the setup and deploy tasks.

## Role Variables

See [defaults/main.yml](./defaults/main.yml) for a full list with available variables.


## Testing

The project comes with Vagrantfile that makes it possible to easily test the role.

Use `vagrant provision/vagrant up` 


## Author

Jyoti Bhanot, <jyoti.bhanot30@gmail.com>


