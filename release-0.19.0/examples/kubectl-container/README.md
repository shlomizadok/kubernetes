This directory contains a Dockerfile and Makefile for packaging up kubectl into
a container.

It's not currently automated as part of a release process, so for the moment
this is an example of what to do if you want to package kubectl into a
container/your pod.

In the future, we may release consistently versioned groups of containers when
we cut a release, in which case the source of gcr.io/google_containers/kubectl
would become that automated process.

```pod.json``` is provided as an example of packaging kubectl as a sidecar
container, and to help you verify that kubectl works correctly in
this configuration.

A possible reason why you would want to do this is to use ```kubectl proxy``` as
a drop-in replacement for the old no-auth KUBERNETES_RO service. The other
containers in your pod will find the proxy apparently serving on localhost.


[![Analytics](https://kubernetes-site.appspot.com/UA-36037335-10/GitHub/examples/kubectl-container/README.md?pixel)]()


[![Analytics](https://kubernetes-site.appspot.com/UA-36037335-10/GitHub/release-0.19.0/examples/kubectl-container/README.md?pixel)]()
