On CentOS 7 HV:

- /var/lib/libvirt/iamges # wget https://download.fedoraproject.org/pub/fedora/linux/releases/39/Server/x86_64/iso/Fedora-Server-dvd-x86_64-39-1.5.iso

- /var/lib/libvirt/iamges # wget https://download.fedoraproject.org/pub/fedora/linux/releases/39/Server/x86_64/iso/Fedora-Server-39-1.5-x86_64-CHECKSUM

- /var/lib/libvirt/iamges # curl -O https://fedoraproject.org/fedora.gpg

- /var/lib/libvirt/iamges # gpg --list-keys --with-fingerprint --keyid-format long --keyring ./fedora.gpg
./fedora.gpg
------------
pub   4096R/DB4639719867C58F 2021-02-04
      Key fingerprint = 787E A6AE 1147 EEE5 6C40  B30C DB46 3971 9867 C58F
uid                          Fedora (35) <fedora-35-primary@fedoraproject.org>

pub   4096R/999F7CBF38AB71F4 2021-02-10
      Key fingerprint = 53DE D2CB 922D 8B8D 9E63  FD18 999F 7CBF 38AB 71F4
uid                          Fedora (36) <fedora-36-primary@fedoraproject.org>

pub   4096R/F55AD3FB5323552A 2021-08-10
      Key fingerprint = ACB5 EE4E 831C 74BB 7C16  8D27 F55A D3FB 5323 552A
uid                          Fedora (37) <fedora-37-primary@fedoraproject.org>

pub   4096R/809A8D7CEB10B464 2022-02-08
      Key fingerprint = 6A51 BBAB BA3D 5467 B617  1221 809A 8D7C EB10 B464
uid                          Fedora (38) <fedora-38-primary@fedoraproject.org>

pub   4096R/75CF5AC418B8E74C 2022-08-09
      Key fingerprint = E8F2 3996 F232 1864 0CB4  4CBE 75CF 5AC4 18B8 E74C
uid                          Fedora (39) <fedora-39-primary@fedoraproject.org>

pub   4096R/0727707EA15B79CC 2023-01-24
      Key fingerprint = 115D F9AE F857 853E E844  5D0A 0727 707E A15B 79CC
uid                          Fedora (40) <fedora-40-primary@fedoraproject.org>

- /var/lib/libvirt/iamges # Rgpgv --keyring ./fedora.gpg Fedora-Server-39-1.5-x86_64-CHECKSUM
gpgv: Signature made Fri 03 Nov 2023 09:51:06 AM CDT using RSA key ID 18B8E74C
gpgv: Good signature from "Fedora (39) <fedora-39-primary@fedoraproject.org>"

- /var/lib/libvirt/iamges # sha256sum -c gpgv --keyring ./fedora.gpg Fedora-Server-39-1.5-x86_64-CHECKSUM
Fedora-Server-dvd-x86_64-39-1.5.iso: OK
sha256sum: Fedora-Server-netinst-x86_64-39-1.5.iso: No such file or directory
Fedora-Server-netinst-x86_64-39-1.5.iso: FAILED open or read

