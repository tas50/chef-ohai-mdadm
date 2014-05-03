chef-ohai-mdadm
===============

A Chef Ohai plugin for gathering mdadm data. This will give you output of all your mdadm software raid volumes in Linux.

##Usage
Install the plugin in your /etc/chef/ohai_plugins direcotry, and add the Ohai cookbook to your runlist to load plugins from that directory.  There are plugins provided for Ohai 6 and Ohai 7.  Make sure to use the appropriate plugin based on your version of Ohai.

###Example Output:

```javascript
"mdadm": {
{
  "md0": {
    "device_counts": {
      "raid": 2,
      "total": 2,
      "active": 2,
      "working": 2,
      "failed": 0,
      "spare": 0
    },
    "metadata_version": "0.9",
    "level": 1,
    "size": 25.01,
    "state": "clean"
  },
  "md1": {
    "device_counts": {
      "raid": 2,
      "total": 2,
      "active": 2,
      "working": 2,
      "failed": 0,
      "spare": 0
    },
    "metadata_version": "1.2",
    "level": 1,
    "size": 16.01,
    "state": "clean"
  }
}

```

License and Author
------------------

Author:: Limelight Networks, Inc. (<tsmith@limelight.com>)

Copyright:: 2013-2014, Limelight Networks, Inc.

License:: Apache 2.0
