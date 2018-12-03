[//]: # "This README.md file is auto-generated, all changes to this file will be lost."
[//]: # "To regenerate it, use `npm run generate-scaffolding`."
<img src="https://avatars2.githubusercontent.com/u/2810941?v=3&s=96" alt="Google Cloud Platform logo" title="Google Cloud Platform" align="right" height="96" width="96"/>

# [Google Cloud OS Login API: Node.js Client](https://github.com/googleapis/nodejs-os-login)

[![release level](https://img.shields.io/badge/release%20level-alpha-orange.svg?style&#x3D;flat)](https://cloud.google.com/terms/launch-stages)
[![npm version](https://img.shields.io/npm/v/@google-cloud/os-login.svg)](https://www.npmjs.org/package/@google-cloud/os-login)
[![codecov](https://img.shields.io/codecov/c/github/googleapis/nodejs-os-login/master.svg?style=flat)](https://codecov.io/gh/googleapis/nodejs-os-login)

> Node.js idiomatic client for [Cloud OS Login API][product-docs].

The [Google Cloud OS Login API](https://cloud.google.com/compute/docs/oslogin/rest) manages OS login configuration for Google account users.


* [Cloud OS Login API Node.js Client API Reference][client-docs]
* [github.com/googleapis/nodejs-os-login](https://github.com/googleapis/nodejs-os-login)
* [Cloud OS Login API Documentation][product-docs]

Read more about the client libraries for Cloud APIs, including the older
Google APIs Client Libraries, in [Client Libraries Explained][explained].

[explained]: https://cloud.google.com/apis/docs/client-libraries-explained

**Table of contents:**

* [Quickstart](#quickstart)
  * [Before you begin](#before-you-begin)
  * [Installing the client library](#installing-the-client-library)
  * [Using the client library](#using-the-client-library)
* [Versioning](#versioning)
* [Contributing](#contributing)
* [License](#license)

## Quickstart

### Before you begin

1.  Select or create a Cloud Platform project.

    [Go to the projects page][projects]

1.  Enable billing for your project.

    [Enable billing][billing]

1.  Enable the Google Cloud OS Login API API.

    [Enable the API][enable_api]

1.  [Set up authentication with a service account][auth] so you can access the
    API from your local workstation.

[projects]: https://console.cloud.google.com/project
[billing]: https://support.google.com/cloud/answer/6293499#enable-billing
[enable_api]: https://console.cloud.google.com/flows/enableapi?apiid=oslogin.googleapis.com
[auth]: https://cloud.google.com/docs/authentication/getting-started

### Installing the client library

    npm install --save @google-cloud/os-login

### Using the client library

```javascript
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

client
  .getLoginProfile(request)
  .then(responses => {
    const loginProfile = responses[0];
    console.log(loginProfile);
  })
  .catch(err => {
    console.error('ERROR:', err);
  });
```


The [Cloud OS Login API Node.js Client API Reference][client-docs] documentation
also contains samples.

## Versioning

This library follows [Semantic Versioning](http://semver.org/).

This library is considered to be in **alpha**. This means it is still a
work-in-progress and under active development. Any release is subject to
backwards-incompatible changes at any time.

More Information: [Google Cloud Platform Launch Stages][launch_stages]

[launch_stages]: https://cloud.google.com/terms/launch-stages

## Contributing

Contributions welcome! See the [Contributing Guide](https://github.com/googleapis/nodejs-os-login/blob/master/.github/CONTRIBUTING.md).

## License

Apache Version 2.0

See [LICENSE](https://github.com/googleapis/nodejs-os-login/blob/master/LICENSE)

[client-docs]: https://cloud.google.com/nodejs/docs/reference/os-login/latest/
[product-docs]: https://cloud.google.com/compute/docs/oslogin/rest
[shell_img]: //gstatic.com/cloudssh/images/open-btn.png

