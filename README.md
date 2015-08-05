# Probe Dock RT Clients

**Documentation and integration guide for [Probe Dock RT](https://github.com/probedock/probedock-rt) clients.**

* [List of Clients](#clients)
* [List of Libraries](#libraries)
* [Setup Procedure](#setup-procedure)
* [Configuration Files](#configuration-files)

<a name="clients"></a>
## List of Clients

Clients exist for the following test frameworks:

* [Junit Client](https://github.com/probedock/probedock-rt-junit) ([demo](https://github.com/probedock/probedock-demo-junit))
* [Java ITF Client](https://github.com/probedock/probedock-rt-itf) ([demo](https://github.com/probedock/probedock-demo-itf))

<a name="libraries"></a>
## List of Libraries

The following libraries can be used to develop new clients:

* [Java](https://github.com/probedock/probedock-rt-java)

<a name="setup-procedure"></a>
## Setup Procedure

This procedure documents the minimal setup for a standard Probe Dock RT client.

Create the `~/.probedock/probedock-rt.yml` configuration file (in your **home directory**).

```yml
host: 127.0.0.1
port: 1337
openBrowser: true
enabled: true
```

Read on to learn about other [configuration properties](#configuration-files).

<a name="configuration-files"></a>
## Configuration Files

Most Probe Dock RT clients use [YAML](http://yaml.org) files for configuration.
The following files will be loaded if they exist:

* the home configuration file: `~/.probedock/probedock-rt.yml`;
* the project configuration file: `/path/to/your/project/probedock.yml`. This file is not mandatory.

**Remark**: When the project configuration file is missing, there is no possibility to get the  `project API ID` or the
project version. Therefore, the value `Any` will be used for both. The result of using this value will make all the test
result notifications gathered by Probe Dock RT will be grouped under a common anonymous project.

### Full Configuration File

Here is an annotated example of a full configuration file.

```yml
# Host and port are used by the clients to send the test result notifications. It is also used 
# to open the browser at the right address when starting Probe Dock RT
host: 127.0.0.1
port: 1337

# By default, when Probe Dock RT is started, the default browser is open to the starting page. This can
# be deactivated by setting this option to false.
openBrowser: true

# By default, running the tests with Probe Dock RT clients configured will send the test result notifications.
# It is possible to deactivate this behavior by setting this option to false.
enabled: true
```

## Contributing

* [Fork](https://help.github.com/articles/fork-a-repo)
* Create a topic branch - `git checkout -b feature`
* Push to your branch - `git push origin feature`
* Create a [pull request](http://help.github.com/pull-requests/) from your branch

Please add a changelog entry with your name for new features and bug fixes.

## License

This guide and its examples are licensed under the [MIT License](http://opensource.org/licenses/MIT).
See [LICENSE.txt](LICENSE.txt) for the full text.
