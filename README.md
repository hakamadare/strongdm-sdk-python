# strongDM SDK for Python

This is the official [strongDM](https://www.strongdm.com/) SDK for the Python
programming language.

Learn more with our [📚strongDM API docs](https://www.strongdm.com/docs/api/) or
[📓browse the SDK
reference](https://strongdm.github.io/strongdm-sdk-python-docs/).

## Installation

```bash
$ pip install strongdm
```

strongDM uses [semantic versioning](https://semver.org/). We do not guarantee
compatibility between major versions. Be sure to use version constraints to pin
your dependency to the desired major version of the strongDM SDK.

## Authentication

If you don't already have them you will need to generate a set of API keys,
instructions are here: [API
Credentials](https://www.strongdm.com/docs/admin-guide/api-credentials/)

Add the keys as environment variables; the SDK will need to access these keys
for every request.
```bash
$ export SDM_API_ACCESS_KEY=<YOUR ACCESS KEY>
$ export SDM_API_SECRET_KEY=<YOUR SECRET KEY>
```

## List Users
The following code lists all registered users:

```python
import os
import strongdm

def main():
    client = strongdm.Client(os.getenv("SDM_API_ACCESS_KEY"),
                        os.getenv("SDM_API_SECRET_KEY"))

    users = client.accounts.list('')
    for user in users:
        print(user)

if __name__ == "__main__":
    main()
```

## Useful Links

* Documentation:  [strongdm package](https://strongdm.github.io/strongdm-sdk-python-docs/)
* [Migrating from Role Grants to Access Rules](https://github.com/strongdm/strongdm-sdk-python/wiki/Migrating-from-Role-Grants-to-Access-Rules)
* Examples: [GitHub - strongdm/strongdm-sdk-python-examples](https://github.com/strongdm/strongdm-sdk-python-examples)
	1. [Managing Resources](https://github.com/strongdm/strongdm-sdk-python-examples/tree/master/1_managing_resources)
	2. [Managing Accounts](https://github.com/strongdm/strongdm-sdk-python-examples/tree/master/2_managing_accounts)
	3. [Managing Roles](https://github.com/strongdm/strongdm-sdk-python-examples/tree/master/3_managing_roles)
	4. [Managing Gateways](https://github.com/strongdm/strongdm-sdk-python-examples/tree/master/4_managing_gateways)
   
## License

[Apache 2](https://github.com/strongdm/strongdm-sdk-python/blob/master/LICENSE)

## Contributing 

Currently, we are not accepting pull requests directly to this repository, but
our users are some of the most resourceful and ambitious folks out there. So, if
you have something to contribute, find a bug, or just want to give us some
feedback, please email <support@strongdm.com>.