---
slug: /privacy
title: Privacy
---

# Privacy

This privacy policy details the data that is collected when you interact with Batect and its related services.

## General principles

As an open source project, the Batect project does not have the resources to run detailed user studies to understand best how to design features or
prioritise work, and instead relies on community feedback and data. We collect data only for the purpose of:

- understanding how the Batect application and its related services ("Batect") are used
- maintaining and improving Batect
- monitoring the security, availability and performance of Batect

Data is not:

- used for advertising purposes
- sold
- shared with others, except in aggregate, anonymous form (eg. the total number of users that used Batect over a 7 day period)

## Documentation site statistical information

This documentation site ([batect.dev](https://batect.dev)) collects anonymous statistical information using Google Analytics.

### What data is collected

Google Analytics collects information such as the following:

- the number of unique users that visit the site
- how often a user returns to the site
- the referrer (eg. if you clicked on a link on a Google search result page, the search term, or if you clicked on a link on a blog post, the URL of the blog post)
- the amount of time spent on each page
- the flow of pages a user visits in a single session (eg. 50% of users that view the home page go to the CLI reference page next)
- the general geographic location (country or city) of the user based on IP address
- the browser-reported language preference
- the type of device being used (eg. phone or computer)
- technical information such as the browser version and operating system version
- performance information such as page load times

Google Analytics expressly [forbids](https://support.google.com/analytics/answer/6366371?hl=en-GB&utm_id=ad) collecting
personally identifiable information. Data is always collected over HTTPS.

The following Google Analytics features are _not_ enabled:

- [Remarketing](https://support.google.com/analytics/answer/2611268?hl=en-GB&utm_id=ad)

- [Advertising Features](https://support.google.com/analytics/answer/3450482?hl=en-GB&utm_id=ad), which includes information such as age, gender
  and interests

- [User-ID](https://support.google.com/analytics/answer/3123662?hl=en-GB&utm_id=ad), which tracks users across devices

- [Google Signals](https://support.google.com/analytics/answer/7532985?hl=en-GB&utm_id=ad), which provides similar features to the above features

### How and why the data is used

This data is used to understand how users use the documentation, identify areas for improvement, identify technical issues and
measure the impact of changes to the documentation.

Data collected from Google Analytics is not combined with data from other sources to attempt to identify users.

Only the primary maintainer of Batect, [Charles Korn](https://github.com/charleskorn) has access to the Google Analytics console for this site.

### How to opt-out

Google provides a [browser add-on](https://tools.google.com/dlpage/gaoptout) that blocks Google Analytics on all sites.

There are also a number of third-party add-ons that can block Google Analytics on a per-site basis.

### How to request for your data to be deleted

Send a request to [privacy@batect.dev](mailto:privacy@batect.dev). Your data will be deleted using the Google Analytics
[User Deletion API](https://developers.google.com/analytics/devguides/config/userdeletion/v3) within 14 days.

## Documentation site error reporting

This documentation site ([batect.dev](https://batect.dev)) collects anonymous error information using [Report URI](https://report-uri.com).

### What data is collected

Report URI is used to collect information about [Content Security Policy (CSP)](https://developer.mozilla.org/en-US/docs/Web/HTTP/CSP#Enabling_reporting),
[Certificate Transparency (CT)](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Expect-CT) and
[Network Error Logging (NEL)](https://developer.mozilla.org/en-US/docs/Web/HTTP/Network_Error_Logging) related errors,
as well as warnings captured through [the Reporting API](https://developers.google.com/web/updates/2018/09/reportingapi).

Depending on the nature of the issue, all or some of the following data is collected:

- the page you were viewing when the issue was detected
- the nature of the issue (eg. CSP violation)
- additional diagnostic information related to the problem (eg. what kind of CSP violation occurred and where in the page it occurred)
- the date and time the issue was encountered
- technical information such as the browser version and operating system version

Personally identifiable information is not collected. Information such as IP addresses may be captured by Report URI for their diagnostic purposes,
but it is not linked to the error reports produced by Report URI.

### How and why the data is used

The data is used to identify issues with the site, including configuration errors or other issues that may prevent users from accessing the site or
using its functionality.

Only the primary maintainer of Batect, [Charles Korn](https://github.com/charleskorn) has access to the Report URI console for this site.

### How to opt-out

This data collection is managed by your browser, and can be disabled in your browser's settings.

### How to request for your data to be deleted

As your data is not linked to users in any way, it is not possible to delete data for a single user.

## Documentation site hosting

This documentation site ([batect.dev](https://batect.dev)) is hosted using Netlify and Cloudflare. Both of these services collect data
to enable them to operate and improve their services, and their respective privacy policies apply to this data.

## Documentation site search

This documentation site ([batect.dev](https://batect.dev)) uses Algolia DocSearch to provide search functionality. Algolia collects data
to enable them to operate and improve their services, and [their privacy policy](https://www.algolia.com/policies/privacy/) applies to this data.

## In-app update notifications

Batect checks for updated versions and displays a reminder to the user if a newer version is available. It automatically checks for updates at most once every 36 hours.

It uses a public, encrypted API hosted by the Batect project on GCP and Cloudflare to check for new versions.
A secure, private GCP project dedicated to the purpose of hosting update information hosts the API.

The source code and configuration for this API is available in the [updates.batect.dev](https://github.com/batect/updates.batect.dev) GitHub repository.

Running `./batect --upgrade` uses the same API in the same way to deliver new versions of Batect.

### What data is collected and how it is used

No personally identifiable information or telemetry information is sent to the API as part of this process.

Basic diagnostic information such as IP addresses may be collected in the API's logs. This information is used solely to administer, maintain and monitor the updates API, and is
not combined with telemetry information or any other information source.

Statistical information (date, time, user agent and performance data) is collected and used to monitor the security, stability, performance and availability of the
service and help understand usage patterns.

The API requires encrypted HTTPS connections.

### How to opt-out

Run Batect with `--no-update-notification` to disable checking for new versions.

Note that running `./batect --upgrade` ignores `--no-update-notification` if it is set, and will always use the updates API to check for a new version.

## File downloads

Batect's wrapper script (`batect` / `batect.cmd`) automatically downloads the appropriate version of Batect when it has not already been downloaded.

It uses a public, encrypted API hosted by the Batect project on GCP and Cloudflare to check for new versions.
A secure, private GCP project dedicated to the purpose of hosting update information hosts the API.

The source code and configuration for this API is available in the [updates.batect.dev](https://github.com/batect/updates.batect.dev) GitHub repository.

### What data is collected and how it is used

No personally identifiable information or telemetry information is sent to the API as part of this process.

Basic diagnostic information such as IP addresses may be collected in the API's logs. This information is used solely to administer, maintain and monitor the updates API, and is
not combined with telemetry information or any other information source.

Statistical information (date, time, user agent and performance data) is collected and used to monitor the security, stability, performance and availability of the
service and help understand usage patterns.

The API requires encrypted HTTPS connections.

### How to opt-out

To opt-out, you must modify the wrapper script to use an alternative download server.

## In-app telemetry

Batect can collect anonymous environment, usage and performance information as it runs.

This information does not include personal or sensitive information such as the names of projects or tasks.

### What data is collected and why

| Name                                                                                                                                                                                                               | Example                                                          | Rationale for collection                                                                                                                                                                                                                                                                |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ---------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Environmental information**                                                                                                                                                                                      |
| Batect version                                                                                                                                                                                                     | `0.51.0`                                                         | Helps correlate and compare results for different versions of Batect                                                                                                                                                                                                                    |
| Batect shell tab completion script version                                                                                                                                                                         | `0.2.0`                                                          | Helps correlate and compare results for different versions of the shell tab completion script                                                                                                                                                                                           |
| OS and version                                                                                                                                                                                                     | `Mac OS X 10.15.4 (x86_64)` or `Ubuntu Linux 20.04 (x86_64)`     | Helps correlate and compare results for different operating systems and OS versions and helps plan compatibility changes for different operating systems (eg. dropping support for an older version of an operating system no longer commonly used)                                     |
| Docker version                                                                                                                                                                                                     | `19.03.8`                                                        | Helps correlate and compare results for different versions of Docker and helps plan compatibility changes for different versions of Docker (eg. dropping support for an older version of Docker no longer commonly used)                                                                |
| Docker daemon experimental mode                                                                                                                                                                                    |                                                                  | Helps correlate and compare results for different versions of Docker and understand potential issues introduced by experimental Docker features                                                                                                                                         |
| JVM version                                                                                                                                                                                                        | `Oracle Corporation Java HotSpot(TM) 64-Bit Server VM 1.8.0_162` | Helps correlate and compare results for different JVMs and helps plan compatibility changes for different JVMs (eg. dropping support for an older version of Java no longer commonly used)                                                                                              |
| Git version                                                                                                                                                                                                        | `2.27.0`                                                         | Helps correlate and compare results for different versions of Git and helps plan compatibility changes for different versions of Git (eg. dropping support for an older version of Git no longer commonly used)                                                                         |
| Shell (value of the `SHELL` environment variable)                                                                                                                                                                  | `bash` or `fish`                                                 | Helps plan and prioritise possible future features (eg. shell tab completion)                                                                                                                                                                                                           |
| Terminal type (value of the `TERM` environment variable)                                                                                                                                                           | `xterm-256color`                                                 | Helps plan and prioritise possible future features (eg. CLI output options)                                                                                                                                                                                                             |
| Whether stdin and stdout are connected to a TTY                                                                                                                                                                    |                                                                  | Helps plan and prioritise possible future features (eg. CLI output options)                                                                                                                                                                                                             |
| Whether Batect believes interactivity (eg. updating text) is supported by the console                                                                                                                              |                                                                  | Helps plan and prioritise possible future features (eg. CLI output options)                                                                                                                                                                                                             |
| Whether Batect believes it is running on a CI tool, and the name of the CI tool                                                                                                                                    | `GitHub Actions`, `CircleCI` or `Jenkins`                        | Helps correlate and compare results for different CI tools, helps plan documentation improvements (eg. adding documentation for commonly used CI tools not yet covered in the documentation), helps plan and prioritise possible future features (eg. closer integration with CI tools) |
| Whether the wrapper script downloaded the current version of Batect for this invocation                                                                                                                            |                                                                  | Helps compare telemetry data with download statistics to determine roughly what proportion of users enable telemetry                                                                                                                                                                    |
| A unique, autogenerated user ID used to correlate information across invocations (a [version 4 randomly-generated UUID](<https://en.wikipedia.org/wiki/Universally_unique_identifier#Version_4_(random)>))         | `00001111-2222-3333-4444-555566667777`                           | Helps correlate results across invocations (eg. how often users use Batect, how quickly users upgrade from one version to another) and helps calculate usage statistics (eg. weekly active users)                                                                                       |
| A unique, autogenerated session ID (a [version 4 randomly-generated UUID](<https://en.wikipedia.org/wiki/Universally_unique_identifier#Version_4_(random)>))                                                       | `00001111-2222-3333-4444-555566667777`                           | Allows easy identification and deduplication of uploaded data                                                                                                                                                                                                                           |
| Time taken to upload telemetry information in the background                                                                                                                                                       | 0.2 seconds                                                      | Helps understand the impact of telemetry collection                                                                                                                                                                                                                                     |
| **Usage information**                                                                                                                                                                                              |
| Command                                                                                                                                                                                                            | running a task, upgrading Batect, displaying help                | Helps segment data (eg. determining average command duration for `--upgrade`) and understand usage behaviour (eg. how often `--help` is used)                                                                                                                                           |
| Exit code                                                                                                                                                                                                          | `0`                                                              | Helps understand whether the invocation succeeded or not                                                                                                                                                                                                                                |
| Time the command started in UTC                                                                                                                                                                                    | `2020-08-10T16:54:00.123Z`                                       | Provides an ordering of invocations, helps determine average time between invocations, and together with other timing values, helps understand the performance of Batect                                                                                                                |
| Time the JVM started in UTC                                                                                                                                                                                        | `2020-08-10T16:54:00.102Z`                                       | Provides an ordering of invocations, helps determine average time between invocations, and together with other timing values, helps understand the performance of Batect                                                                                                                |
| Time the command finished in UTC                                                                                                                                                                                   | `2020-08-10T16:54:03.423Z`                                       | Provides an ordering of invocations, helps determine average time between invocations, and together with other timing values, helps understand the performance of Batect                                                                                                                |
| Output mode used                                                                                                                                                                                                   | `simple`, `fancy`, `quiet` or `all`                              | Helps understand usage behaviour and helps plan and prioritise possible future features                                                                                                                                                                                                 |
| Whether `--no-color` is enabled                                                                                                                                                                                    |                                                                  | Helps understand usage behaviour and helps plan and prioritise possible future features                                                                                                                                                                                                 |
| Docker connection type                                                                                                                                                                                             | Unix socket, Windows named pipe or TCP                           | Helps understand usage behaviour and helps plan and prioritise possible future features                                                                                                                                                                                                 |
| Whether `--docker-tls` or `--docker-tls-verify` is set                                                                                                                                                             |                                                                  | Helps understand usage behaviour and helps plan and prioritise possible future features                                                                                                                                                                                                 |
| Whether a custom configuration file name (ie. not `batect.yml`) is being used                                                                                                                                      | `false`                                                          | Helps understand usage behaviour and helps plan and prioritise possible future features                                                                                                                                                                                                 |
| Whether a config variables file is being used                                                                                                                                                                      | `true`                                                           | Helps understand usage behaviour and helps plan and prioritise possible future features                                                                                                                                                                                                 |
| Whether the following features have been disabled: update notifications, wrapper cache cleanup, cleanup after success, cleanup after failure, proxy environment variable propagation, maximum level of parallelism |                                                                  | Helps understand usage behaviour and helps plan and prioritise possible future features                                                                                                                                                                                                 |
| Whether a 'new Batect version available' notification is shown                                                                                                                                                     |                                                                  | Helps understand usage behaviour and helps plan and prioritise possible future features (eg. tools to help upgrade Batect automatically)                                                                                                                                                |
| **Task run information**                                                                                                                                                                                           |
| Type of container being run                                                                                                                                                                                        | Windows or Linux                                                 | Helps understand usage behaviour and helps plan and prioritise possible future features                                                                                                                                                                                                 |
| Docker daemon's preferred image builder                                                                                                                                                                            | Legacy or BuildKit                                               | Helps understand usage behaviour and helps plan and prioritise possible future features                                                                                                                                                                                                 |
| Image builder in use                                                                                                                                                                                               | Legacy or BuildKit                                               | Helps understand usage behaviour and helps plan and prioritise possible future features                                                                                                                                                                                                 |
| Type of cache being used                                                                                                                                                                                           | volume or directory                                              | Helps understand usage behaviour and helps plan and prioritise possible future features                                                                                                                                                                                                 |
| Total number of tasks in the project                                                                                                                                                                               | 10                                                               | Helps understand usage behaviour and helps plan and prioritise possible future features (eg. performance improvements for very large projects)                                                                                                                                          |
| Total number of containers in the project                                                                                                                                                                          | 4                                                                | Helps understand usage behaviour and helps plan and prioritise possible future features (eg. performance improvements for very large projects)                                                                                                                                          |
| Total number of configuration variables in the project                                                                                                                                                             | 6                                                                | Helps understand usage behaviour and helps plan and prioritise possible future features (eg. performance improvements for very large projects)                                                                                                                                          |
| Total number of prerequisite tasks required to execute before executing the main task                                                                                                                              | 2                                                                | Helps understand usage behaviour and helps plan and prioritise possible future features (eg. performance improvements for very large projects)                                                                                                                                          |
| Number of config variable overrides specified on the command line                                                                                                                                                  | 0                                                                | Helps understand usage behaviour and helps plan and prioritise possible future features                                                                                                                                                                                                 |
| Number of image overrides specified on the command line                                                                                                                                                            | 1                                                                | Helps understand usage behaviour and helps plan and prioritise possible future features                                                                                                                                                                                                 |
| Whether an existing Docker network was specified on the command line                                                                                                                                               | `false`                                                          | Helps understand usage behaviour and helps plan and prioritise possible future features                                                                                                                                                                                                 |
| Whether prerequisites were skipped on the command line                                                                                                                                                             | `false`                                                          | Helps understand usage behaviour and helps plan and prioritise possible future features                                                                                                                                                                                                 |
| Number of additional arguments passed on the command line to the task                                                                                                                                              | 2                                                                | Helps understand usage behaviour and helps plan and prioritise possible future features                                                                                                                                                                                                 |
| Number of containers started for each task                                                                                                                                                                         | 3                                                                | Helps understand usage behaviour and helps plan and prioritise possible future features (eg. performance improvements for very large projects)                                                                                                                                          |
| Time taken to load the configuration for the project                                                                                                                                                               | 0.05 seconds                                                     | Helps understand usage and application behaviour and helps plan and prioritise possible future features (eg. performance improvements for very large projects)                                                                                                                          |
| Time taken to execute each task                                                                                                                                                                                    | 3.3 seconds                                                      | Helps understand usage and application behaviour and helps plan and prioritise possible future features (eg. performance improvements for very large projects)                                                                                                                          |
| Time taken to execute each step in each task (eg. pulling or building an image, creating a container, stopping a container, removing a container)                                                                  | 0.4 seconds                                                      | Helps understand usage and application behaviour and helps plan and prioritise possible future features (eg. performance improvements for certain steps)                                                                                                                                |
| **Exception information**                                                                                                                                                                                          |
| Type of exception                                                                                                                                                                                                  | `IOException` or `ContainerCreationFailedException`              | Helps understand possible bugs, helps understand the frequency with which users see certain classes of errors and helps plan and prioritise possible future features (eg. recovering from errors automatically or suggesting recovery actions to the user)                              |
| Stack trace                                                                                                                                                                                                        |                                                                  | Helps understand possible bugs, helps understand the frequency with which users see certain classes of errors and helps plan and prioritise possible future features (eg. recovering from errors automatically or suggesting recovery actions to the user)                              |
| Whether the exception was user-facing or not (eg. occurred in a cache cleanup background task)                                                                                                                     | `false`                                                          | Helps understand possible bugs, helps understand the frequency with which users see certain classes of errors and helps plan and prioritise possible future features (eg. recovering from errors automatically or suggesting recovery actions to the user)                              |

### What data is not collected

As a rule, any personally-identifiable or potentially sensitive information is not collected, including:

- personally-identifiable information, such as user names or email addresses
- IP addresses (IP addresses may be captured in request logs, but IP addresses are not associated with uploaded data)
- names of projects, containers, tasks or config variables
- environment variable names or values, with the exception of `TERM` and `SHELL`
- names of Docker images used
- names of files
- any part of task command lines
- exception messages, as these cannot be guaranteed to contain only non-sensitive information
- timezone information (all timestamps collected are normalised to UTC before upload)

### How data is used

Data is used in accordance with the [general principles above](#general-principles) - to understand how Batect is used, to maintain Batect, to monitor its
performance and reliability, and improve it.

### How data is collected and stored

Data is collected as the application runs, and then uploaded to a secure, private GCP project dedicated to storing and processing this information.

All data is transferred over HTTPS, and encrypted at rest. A variety of controls are in place to ensure that raw data is not disclosed publicly.

### Who has access to the data

Only the primary maintainer of Batect, [Charles Korn](https://github.com/charleskorn) has access to this data once it is uploaded.

Aggregated, anonymous information (eg. the total number of users that used Batect over a 7 day period) may be shared with others.

### How to opt-out

When Batect starts for the first time, it prompts for permission to collect this information:

```text
Batect can collect anonymous environment, usage and performance information.
This information does not include personal or sensitive information, and is used only to help improve Batect.
More information is available at https://batect.dev/privacy, including details of what information is collected and a formal privacy policy.

Is it OK for Batect to collect this information? (Y/n)
```

To opt-out, respond with `no`.

To opt-out after this initial run, do any of the following:

- Run [`./batect --permanently-disable-telemetry`](/docs/reference/cli#--permanently-disable-telemetry) once, which disables telemetry
  and deletes any data that has been collected but not yet uploaded

- Run each task with [`./batect --no-telemetry <task>`](/docs/reference/cli#--no-telemetry) (eg. `./batect --no-telemetry build`),
  which disables telemetry for that invocation of Batect

- Set the `BATECT_ENABLE_TELEMETRY` environment variable to `false`

- Set [`forbid_telemetry`](/docs/reference/config#forbid_telemetry) to `true` in your project's configuration file

If you wish to block telemetry data uploads at the network level, block access to `api.abacus.batect.dev`. Note that the IP address of this host name
can change at any time, so it is best to block the host name, not the IP address. (Do not block access to `batect.dev`, as that will block access to this site.)

### How to request for your data to be deleted

Send a request to [privacy@batect.dev](mailto:privacy@batect.dev), and include your user ID from `~/.batect/telemetry/config.json`. Your data will be deleted
within 14 days.

## Third-party services

The Batect project uses a number of third-party services such as GitHub for code hosting.

When you interact with these services, their respective privacy policy applies.
