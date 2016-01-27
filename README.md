# datastore.cloudfiles

[Rackspace Cloud Files](https://www.rackspace.com/cloud/files/) implementation of [Datastore](https://github.com/datastore/datastore).


## Install

From PyPI (using pip):

```sh
pip install datastore.cloudfiles
```

From PyPI (using setuptools):

```sh
easy_install datastore.aws
```

From source:

```sh
git clone https://github.com/boilerroomtv/datastore.cloudfiles
cd datastore.cloudfiles
python setup.py install
```


## Quickstart

```python
>>> import datastore.cloudfiles
>>> import pyrax
>>>
>>> pyrax.set_setting('identity_type', 'rackspace')
>>> pyrax.set_default_region(RACKSPACE_REGION)
>>> pyrax.set_credentials(RACKSPACE_USERNAME, RACKSPACE_API_KEY)
>>> container = pyrax.cloudfiles.create_container(self.container_name)
>>> ds = datastore.cloudfiles.RackspaceCloudFilesDatastore(self.container)
>>>
>>> hello = datastore.Key('hello')
>>> ds.put(hello, 'world')
>>> ds.contains(hello)
True
>>> ds.get(hello)
'world'
>>> ds.delete(hello)
>>> ds.get(hello)
None
```


## License

Original code in `datastore.cloudfiles` is licensed under the [Mozilla Public License 2.0](https://www.mozilla.org/en-US/MPL/2.0/).
