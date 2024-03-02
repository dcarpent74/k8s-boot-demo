# k8s-boot-demo
## Kubernetes Bootstrap Demonstration

I want to start here a documentation bootstrap.  This is baking from scratch,
so I want to describe my starting place and proceed from the ground up. I know
there are fancier ways to do this with less effort, but most tooling requires
learning to use.  I am starting with what is familiar to me, learning stuff
that seems like an easy path for my goal, and leveraging what I already know
well.

So a quick outline of what I know well:
* Red Hat style distributions especially from the early days.
* RPM, rpmbuild, etc... Learned on Red Hat 5.x - 9 (free late 90's-2000's stuff)
* Honed Red Hat / RPM deployment skills on RHEL 2.1 - 4 and RH Satellite server.
* Production build engineer for mostly O/S and systems middleware products.
* C and bash (lots of Korn to, but I prefer bash).
* Networking, VMWare ESXi and Linux/KVM/qemu/libvirt virtualization.
* LVM, Unix file-systems internals (more old-school stuff).
* DevOps style process stuff.  Cut my teeth on mid-1990's Intel style Kaizen.

So here is where I am going to start...  I have a CentOS 7 system that has a
basic hypervisor setup and a OpenSUSE Leap 15.5 hypervisor even less setup, but
enough to launch a few demo VMs. My CentOS box is really intended to be a more
real hypervisor.  it is an Xeon D-1541 8 core server with 10GB and 1 GB NICs and
a bunch of RAM and about 28 TB of 7200 RPM storage. My OpenSUSE system is an
L5640 server recently updated to 24 GB or RAM, and over 100 TB of 7200 RPM disk
(a gang of 18TB NAS drives.  This system also has networking upgrades similar to
my newer server.  The primary intent for this system is to serve as a archival
backup server, but for other light and mostly CPU oriented tasks, I can keep the
CPUs occupied with some other stuff.  Hopefully, there are a couple more of
these same systems in the works soon.

For the moment, I will begin my initial work on the CentOS system, and since I
do not want to terribly disrupt its previous life just yet, I will be starting
with a fairly vanilla Fedora VM set up on top. At the moment my newer bare metal
installs are probably going to be OpenSUSE Leap 15.5/latest until I decide I
am less in need of a long term stable stable hypervisor platform. That may
change again soon as I am not entirely happy with SUSE either, but the latest
CentOS debacle has scared me away from CentOS and I am undecided in terms of
ALMA or Rocky. Honestly at this point I wish I were more of a Debian person. I
am using Mint Linux for Desktop these days and pretty happy with it other than
the fact that I still struggle with not knowing deb packaging to the level that
I know RPM. I worked on that for a little bit, but mostly felt like I was
banging my head against the wall.

I have some history with Fedora too, but honestly, I just felt like the upgrade
and update cycles were just too much, and Fedora in the past was not quite
stable enough for me. The pain of moving forward for my workflow on Fedora drove
me to CentOS almost exclusively.  Even that pace on Mint is a little faster than
I'd like, but that is part of why I am here.

My objectives:
* Figure out a way to have easy bare metal installation and upgrades.
* Figure out a way to have a nice desktop that I like, but that does not have
a typical bare-metal story.
  * Manage my personal data in a private but more cloud centered manner.
  * Have some method/workflow to capture my desktop such that I can have a more
painless upgrade cycle.
  * Have a way to easily track and reproduce my core Desktop configuration
settings as my Desktop
  * Continue moving some of my more persistent desktop "work" to solutions like
my VNC desktop servers so work can live more independent of my desktop.
platform evolves.
  * Figure out a better way to manage browser bookmarks, tabs, tab groups, and
windows (but may be not getting on some plugin bandwagon).
* Set up a system for distributed storage, VM migration, and probably move some
of my needs into Kubernetes.
* Kubernetes should also be easy to install / upgrade (something akin to Talos
Linux seems desirable to me, but for the moment I want more vanilla K8s to learn
on).
* To these ends, I think I need to establish the following services in my
environment:
  * Kubernetes
  * Git based SCM (OneDev or GitLab seem like options).
  * Ceph / Rook (or something that gives me similar results.
* While I like the more stateless stuff, I also want more persistent state for
some of what I do.  I still like my desktop and work terminals and such to stay
open and running 24/7.

The Fedora VM:

So the point of the Fedora VM at this point is to have relatively easy admin
console. Without SCM or other more distributed storage, I want to start by
bootstrapping everything from here.

A big part of the bootstrap process is documentation, which I will be pushing
here (to GitHub).

In lieu of SCM, I can start some git repositories on this Fedora system.  I
should organize such that it is easy to backup my local data to the backup
server, deploy a new Fedora VM and restore and keep going. To this end, maybe
I will initially set up this as a nested hypervisor to prototype easy deploys
for this VM. Long term the admin console might be a VM or might be special
container thing. Whatever that is, I should be able to have this up and running
pretty easily from bare metal and with little effort. Fedora VM template and
backup restore. Fedora template VM with podman and container thingy. Maybe
eventually have podman on the desktop / bare metal systems and launch from
there?

While I am focusing less on the desktop right now, I want to set up some of the
infrastructure to do easier deploys of whatever at home.  This should be a
path to having that stuff.

I also want to do the multiple recursion loop on this documentation (DevOps
bootstrap style).  I am documenting based on my current notions, and as I learn
updating / improving the documentation.  That means, maintaining a history (this
is why GitHub for Documentation in the first place), a historical document that
should cover the basics of the learning process, a document that describes the
mature bootstrap process (think reproducible and proven DR, improved through
itteration), and a document that is maintained describes the current system and
it use as currently implemented.

So this will become the first history document, but it also represents this
moment in time with a synopsis of what I have running, little to nothing new
implemented, and just a vision of where I want things to go.
