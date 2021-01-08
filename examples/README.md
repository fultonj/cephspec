# Example Spec Files

All of these spec files have been tested on a single bootstrap
system. For example:

```
[root@oc0-ceph-1 ~]# cephadm shell
[ceph: root@oc0-ceph-1 /]# ceph orch apply -i add_host.yaml 
Added host 'oc0-ceph-2'
[ceph: root@oc0-ceph-1 /]#
```

[add_host.yaml](add_host.yaml) assumes that the same SSH keys are 
in place which were used to bootstrap the node where spec is applied.
It adds another ceph-mgr on that host but not another ceph-mon.

You can then add a mon to the host which added
with [add_mon.yaml](add_mon.yaml):

```
[ceph: root@oc0-ceph-1 /]# ceph orch apply -i add_mon.yaml 
Scheduled mon update...
[ceph: root@oc0-ceph-1 /]#
```

You can then add OSDs using [add_osds.yaml](add_osds.yaml):

```
[ceph: root@oc0-ceph-1 /]# ceph orch apply -i add_osds.yaml 
Scheduled osd.default_drive_group update...
[ceph: root@oc0-ceph-1 /]# 
```

You can also extract what has been generated with `ceph orch ls
--export`.
