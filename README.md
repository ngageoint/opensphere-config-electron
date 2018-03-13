# OpenSphere Electron Configuration

Provides OpenSphere configuration specific to Electron builds. This project should be cloned alongside [`opensphere`](https://github.com/ngageoint/opensphere) and [`opensphere-electron`](https://github.com/ngageoint/opensphere-electron).

These settings are primarily intended to:
* Disable the proxy: CORS has been disabled in `opensphere-electron`, so a proxy is not needed for network requests.
* Enable mixed content: Electron can access the local file system via `file://` URL's, as well as remote resources.
* Provide a scheme for network-path references: URL's beginning with `//` are intended to use the app's URL scheme, but for Electron that will be `file://` and break the URL.
