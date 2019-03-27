[//]: # "This README.md file is auto-generated, all changes to this file will be lost."
[//]: # "To regenerate it, use `python -m synthtool`."
<img src="https://avatars2.githubusercontent.com/u/2810941?v=3&s=96" alt="Google Cloud Platform logo" title="Google Cloud Platform" align="right" height="96" width="96"/>

# [:  Client](https://github.com/)

None
[![npm version](https://img.shields.io/npm/v/@google-cloud/os-login.svg)](https://www.npmjs.org/package/@google-cloud/os-login)
[![codecov](https://img.shields.io/codecov/c/github//master.svg?style=flat)](https://codecov.io/gh/)


Google Cloud OS Login API client for Node.js


* [Using the client library](#using-the-client-library)
* [Versioning](#versioning)
* [Contributing](#contributing)
* [License](#license)

## Using the client library

1.  [Select or create a Cloud Platform project][projects].
1.  [Enable the  API][enable_api].
1.  [Set up authentication with a service account][auth] so you can access the
    API from your local workstation.

1. Install the client library:

        npm install @google-cloud/os-login


1. Try an example:

```
  if (
    !process.env.GCLOUD_PROJECT ||
    !process.env.GOOGLE_APPLICATION_CREDENTIALS
  ) {
    throw new Error(
      'Usage: GCLOUD_PROJECT=<project_id> GOOGLE_APPLICATION_CREDENTIALS=<path to key json file> node #{$0}'
    );
  }

  const oslogin = require('@google-cloud/os-login');

  const projectId = process.env.GCLOUD_PROJECT;

  const client = new oslogin.OsLoginServiceClient({
    projectId: projectId,
  });

  const request = {
    name: 'users/1234abcd',
  };

  const [loginProfile] = await client.getLoginProfile(request);
  console.log(loginProfile);

```




The [  Client API Reference][client-docs] documentation
also contains samples.

## Versioning

This library follows [Semantic Versioning](http://semver.org/).






More Information: [Google Cloud Platform Launch Stages][launch_stages]

[launch_stages]: https://cloud.google.com/terms/launch-stages

## Contributing

Contributions welcome! See the [Contributing Guide](https://github.com//blob/master/CONTRIBUTING.md).

## License

Apache Version 2.0

See [LICENSE](https://github.com//blob/master/LICENSE)

## What's Next

* [ Documentation][product-docs]
* [  Client API Reference][client-docs]
* [github.com/](https://github.com/)

Read more about the client libraries for Cloud APIs, including the older
Google APIs Client Libraries, in [Client Libraries Explained][explained].

[explained]: https://cloud.google.com/apis/docs/client-libraries-explained

[client-docs]: 
[product-docs]: 
[shell_img]: https://gstatic.com/cloudssh/images/open-btn.png
[projects]: https://console.cloud.google.com/project
[billing]: https://support.google.com/cloud/answer/6293499#enable-billing
[enable_api]: https://console.cloud.google.com/flows/enableapi?apiid=
[auth]: https://cloud.google.com/docs/authentication/getting-started