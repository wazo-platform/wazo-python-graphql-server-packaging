# wazo-python-graphql-server-packaging

Debian packaging for [python3-graphql-server](https://github.com/graphql-python/graphql-server/) used in Wazo.

## Upgrading

To upgrade python-graphql-server

* Update the version number in the `VERSION` file
* Update the changelog using `dch -i` to the matching version
* Refresh patches
* Push the changes

## Building Locally

To build on a test environment before submitting a change to production the following procedure can be used.

```sh
debian/rules get-orig-source
tar -xvf ../wazo-python-graphql-server-packaging_*.orig.tar.gz --strip 1
dpkg-buildpackage -us -uc
```
The `.deb` will be located in the parent directory.
