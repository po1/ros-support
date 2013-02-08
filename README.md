### Thoughts on how to structure a repository for ros-support libraries.

1. The ros-support repo is intended as one of the repositories that the building repo pulls updates from; it includes the non-ROS packages we maintain that exist outside of the Ubuntu tree.
1. The ros-support repo should contain sources for all of the packages it contains; this makes it possible to download the sources and compile them for new platforms as appropriate
1. The core repo with sources and supported builds lives on a WG server; satellite repos may exist on outside servers with unsupported or experimental builds.


### Tools to make it easier to build packages: the ros-support github project.

The tools in the ros-support project should make it easy to bring up the support libraries for ROS on a new platform. This means having tools for:

1. Setting up a local reprepro repository for testing.
1. Pulling down sources for all of the known support debs
1. Building all of the local sources for the specified architecture
1. Uploading built debs to the local repo.
1. A script to tar up built debs for submission to the core repository.
1. A script to wrap 2-4
