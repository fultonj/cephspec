# cephspec
cephadm spec examples

## overview

The ability to run

`cephadm bootstrap: add --apply-spec <cluster.yaml>`

Was tracked in
[https://tracker.ceph.com/issues/44873](https://tracker.ceph.com/issues/44873) 
and implemented in
[https://github.com/ceph/ceph/pull/34879](https://github.com/ceph/ceph/pull/34879).
We also have the following sources

- [orchestrator service spec documentation](https://docs.ceph.com/en/latest/mgr/orchestrator/#orchestrator-cli-service-spec)
- [osd service spec documentation](https://docs.ceph.com/en/latest/cephadm/drivegroups/)
- [github doc directory](https://github.com/ceph/ceph/tree/master/doc/cephadm)
- [OSP MVP BZ 1839168](https://bugzilla.redhat.com/show_bug.cgi?id=1839168#c1)

My plan is to pass various sources of input described in the
[tripleo-ceph spec](https://specs.openstack.org/openstack/tripleo-specs/specs/wallaby/tripleo-ceph.html#ceph-end-state-definition-yaml-input)
to a program which creates a valid `cluster.yaml` as output covering
the necessary TripleO scenarios. I'll start with some hands on example
output files of various use cases necessary for TripleO.
