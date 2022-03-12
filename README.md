# policy-peoplefinder

This repository houses the Aserto policy for the PeopleFinder sample.

## Directory structure

`src` contains all the policy files. 

`src/.manifest` contains the policy roots - in this case, `peoplefinder`. If you change the name of the `package` definitions in the `.rego` files, make sure that the first component of the package name is reflected in this list.

`src/policies` contains the policy modules associated with the peoplefinder sample:

* get.rego - `peoplefinder.GET.api.users` - policy for `GET /api/users`
* post.rego - `peoplefinder.POST.api.users` - policy for `POST /api/users`
* __id/delete.rego - `peoplefinder.DELETE.api.users.__id` - policy for `DELETE /api/users/{id}`
* __id/get.rego - `peoplefinder.GET.api.users.__id` - policy for `GET /api/users/{id}`
* __id/post.rego - `peoplefinder.POST.api.users.__id` - policy for `POST /api/users/{id}`
* __id/put.rego - `peoplefinder.PUT.api.users.__id` - policy for `PUT /api/users/{id}`

## Releasing a new version

`git tag {version}` will invoke the actions to create a new release (a policy bundle that can be delivered to the Aserto authorizer)

e.g. `git tag v0.0.1` will create a new release with v0.0.1.
