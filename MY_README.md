скопировал https://github.com/erlong15/otus-linux в свой гитхаб

В командной строке C:\Users\...\Documents\GitHub\otus-linux>


в файл Vagrantfile добавил секцию с новыс диском



```
:sata5 => {
                        :dfile => './sata5.vdi',
                        :size => 1500, # Megabytes
                        :port => 5
                }
```




C:\Users\...\Documents\GitHub\otus-linux>vagrant up

```
==> vagrant: A new version of Vagrant is available: 2.2.9 (installed version: 2.2.7)!
==> vagrant: To upgrade visit: https://www.vagrantup.com/downloads.html

Bringing machine 'otuslinux' up with 'virtualbox' provider...
==> otuslinux: Box 'centos/7' could not be found. Attempting to find and install...
    otuslinux: Box Provider: virtualbox
    otuslinux: Box Version: >= 0
==> otuslinux: Loading metadata for box 'centos/7'
    otuslinux: URL: https://vagrantcloud.com/centos/7
==> otuslinux: Adding box 'centos/7' (v1905.1) for provider: virtualbox
    otuslinux: Downloading: https://vagrantcloud.com/centos/boxes/7/versions/1905.1/providers/virtualbox.box
    otuslinux: Download redirected to host: cloud.centos.org
    otuslinux:
==> otuslinux: Successfully added box 'centos/7' (v1905.1) for 'virtualbox'!
==> otuslinux: Importing base box 'centos/7'...
==> otuslinux: Matching MAC address for NAT networking...
==> otuslinux: Checking if box 'centos/7' version '1905.1' is up to date...
==> otuslinux: Setting the name of the VM: otus-linux_otuslinux_1589035468054_93007
==> otuslinux: Clearing any previously set network interfaces...
==> otuslinux: Preparing network interfaces based on configuration...
    otuslinux: Adapter 1: nat
    otuslinux: Adapter 2: hostonly
==> otuslinux: Forwarding ports...
    otuslinux: 22 (guest) => 2222 (host) (adapter 1)
==> otuslinux: Running 'pre-boot' VM customizations...
==> otuslinux: Booting VM...
==> otuslinux: Waiting for machine to boot. This may take a few minutes...
    otuslinux: SSH address: 127.0.0.1:2222
    otuslinux: SSH username: vagrant
    otuslinux: SSH auth method: private key
    otuslinux:
    otuslinux: Vagrant insecure key detected. Vagrant will automatically replace
    otuslinux: this with a newly generated keypair for better security.
    otuslinux:
    otuslinux: Inserting generated public key within guest...
    otuslinux: Removing insecure key from the guest if it's present...
    otuslinux: Key inserted! Disconnecting and reconnecting using new SSH key...
==> otuslinux: Machine booted and ready!
[otuslinux] No Virtualbox Guest Additions installation found.
Loaded plugins: fastestmirror
Loading mirror speeds from cached hostfile
 * base: mirror.ams1.nl.leaseweb.net
 * extras: centos.mirror.transip.nl
 * updates: mirror.wd6.net
Resolving Dependencies
--> Running transaction check
---> Package centos-release.x86_64 0:7-6.1810.2.el7.centos will be updated
---> Package centos-release.x86_64 0:7-8.2003.0.el7.centos will be an update
--> Finished Dependency Resolution

Dependencies Resolved

================================================================================
 Package              Arch         Version                     Repository  Size
================================================================================
Updating:
 centos-release       x86_64       7-8.2003.0.el7.centos       base        26 k

Transaction Summary
================================================================================
Upgrade  1 Package

Total download size: 26 k
Downloading packages:
No Presto metadata available for base
Public key for centos-release-7-8.2003.0.el7.centos.x86_64.rpm is not installed
warning: /var/cache/yum/x86_64/7/base/packages/centos-release-7-8.2003.0.el7.centos.x86_64.rpm: Header V3 RSA/SHA256 Signature, key ID f4a80eb5: NOKEY
Retrieving key from file:///etc/pki/rpm-gpg/RPM-GPG-KEY-CentOS-7
Importing GPG key 0xF4A80EB5:
 Userid     : "CentOS-7 Key (CentOS 7 Official Signing Key) <security@centos.org>"
 Fingerprint: 6341 ab27 53d7 8a78 a7c2 7bb1 24c6 a8a7 f4a8 0eb5
 Package    : centos-release-7-6.1810.2.el7.centos.x86_64 (@anaconda)
 From       : /etc/pki/rpm-gpg/RPM-GPG-KEY-CentOS-7
Running transaction check
Running transaction test
Transaction test succeeded
Running transaction
  Updating   : centos-release-7-8.2003.0.el7.centos.x86_64                  1/2
  Cleanup    : centos-release-7-6.1810.2.el7.centos.x86_64                  2/2
  Verifying  : centos-release-7-8.2003.0.el7.centos.x86_64                  1/2
  Verifying  : centos-release-7-6.1810.2.el7.centos.x86_64                  2/2

Updated:
  centos-release.x86_64 0:7-8.2003.0.el7.centos

Complete!
Loaded plugins: fastestmirror
Loading mirror speeds from cached hostfile
 * base: mirror.ams1.nl.leaseweb.net
 * extras: centos.mirror.transip.nl
 * updates: mirror.wd6.net
Resolving Dependencies
--> Running transaction check
---> Package kernel-devel.x86_64 0:3.10.0-957.12.2.el7 will be installed
--> Processing Dependency: perl for package: kernel-devel-3.10.0-957.12.2.el7.x86_64
--> Running transaction check
---> Package perl.x86_64 4:5.16.3-295.el7 will be installed
--> Processing Dependency: perl-libs = 4:5.16.3-295.el7 for package: 4:perl-5.16.3-295.el7.x86_64
--> Processing Dependency: perl(Socket) >= 1.3 for package: 4:perl-5.16.3-295.el7.x86_64
--> Processing Dependency: perl(Scalar::Util) >= 1.10 for package: 4:perl-5.16.3-295.el7.x86_64
--> Processing Dependency: perl-macros for package: 4:perl-5.16.3-295.el7.x86_64
--> Processing Dependency: perl-libs for package: 4:perl-5.16.3-295.el7.x86_64
--> Processing Dependency: perl(threads::shared) for package: 4:perl-5.16.3-295.el7.x86_64
--> Processing Dependency: perl(threads) for package: 4:perl-5.16.3-295.el7.x86_64
--> Processing Dependency: perl(constant) for package: 4:perl-5.16.3-295.el7.x86_64
--> Processing Dependency: perl(Time::Local) for package: 4:perl-5.16.3-295.el7.x86_64
--> Processing Dependency: perl(Time::HiRes) for package: 4:perl-5.16.3-295.el7.x86_64
--> Processing Dependency: perl(Storable) for package: 4:perl-5.16.3-295.el7.x86_64
--> Processing Dependency: perl(Socket) for package: 4:perl-5.16.3-295.el7.x86_64
--> Processing Dependency: perl(Scalar::Util) for package: 4:perl-5.16.3-295.el7.x86_64
--> Processing Dependency: perl(Pod::Simple::XHTML) for package: 4:perl-5.16.3-295.el7.x86_64
--> Processing Dependency: perl(Pod::Simple::Search) for package: 4:perl-5.16.3-295.el7.x86_64
--> Processing Dependency: perl(Getopt::Long) for package: 4:perl-5.16.3-295.el7.x86_64
--> Processing Dependency: perl(Filter::Util::Call) for package: 4:perl-5.16.3-295.el7.x86_64
--> Processing Dependency: perl(File::Temp) for package: 4:perl-5.16.3-295.el7.x86_64
--> Processing Dependency: perl(File::Spec::Unix) for package: 4:perl-5.16.3-295.el7.x86_64
--> Processing Dependency: perl(File::Spec::Functions) for package: 4:perl-5.16.3-295.el7.x86_64
--> Processing Dependency: perl(File::Spec) for package: 4:perl-5.16.3-295.el7.x86_64
--> Processing Dependency: perl(File::Path) for package: 4:perl-5.16.3-295.el7.x86_64
--> Processing Dependency: perl(Exporter) for package: 4:perl-5.16.3-295.el7.x86_64
--> Processing Dependency: perl(Cwd) for package: 4:perl-5.16.3-295.el7.x86_64
--> Processing Dependency: perl(Carp) for package: 4:perl-5.16.3-295.el7.x86_64
--> Processing Dependency: libperl.so()(64bit) for package: 4:perl-5.16.3-295.el7.x86_64
--> Running transaction check
---> Package perl-Carp.noarch 0:1.26-244.el7 will be installed
---> Package perl-Exporter.noarch 0:5.68-3.el7 will be installed
---> Package perl-File-Path.noarch 0:2.09-2.el7 will be installed
---> Package perl-File-Temp.noarch 0:0.23.01-3.el7 will be installed
---> Package perl-Filter.x86_64 0:1.49-3.el7 will be installed
---> Package perl-Getopt-Long.noarch 0:2.40-3.el7 will be installed
--> Processing Dependency: perl(Pod::Usage) >= 1.14 for package: perl-Getopt-Long-2.40-3.el7.noarch
--> Processing Dependency: perl(Text::ParseWords) for package: perl-Getopt-Long-2.40-3.el7.noarch
---> Package perl-PathTools.x86_64 0:3.40-5.el7 will be installed
---> Package perl-Pod-Simple.noarch 1:3.28-4.el7 will be installed
--> Processing Dependency: perl(Pod::Escapes) >= 1.04 for package: 1:perl-Pod-Simple-3.28-4.el7.noarch
--> Processing Dependency: perl(Encode) for package: 1:perl-Pod-Simple-3.28-4.el7.noarch
---> Package perl-Scalar-List-Utils.x86_64 0:1.27-248.el7 will be installed
---> Package perl-Socket.x86_64 0:2.010-5.el7 will be installed
---> Package perl-Storable.x86_64 0:2.45-3.el7 will be installed
---> Package perl-Time-HiRes.x86_64 4:1.9725-3.el7 will be installed
---> Package perl-Time-Local.noarch 0:1.2300-2.el7 will be installed
---> Package perl-constant.noarch 0:1.27-2.el7 will be installed
---> Package perl-libs.x86_64 4:5.16.3-295.el7 will be installed
---> Package perl-macros.x86_64 4:5.16.3-295.el7 will be installed
---> Package perl-threads.x86_64 0:1.87-4.el7 will be installed
---> Package perl-threads-shared.x86_64 0:1.43-6.el7 will be installed
--> Running transaction check
---> Package perl-Encode.x86_64 0:2.51-7.el7 will be installed
---> Package perl-Pod-Escapes.noarch 1:1.04-295.el7 will be installed
---> Package perl-Pod-Usage.noarch 0:1.63-3.el7 will be installed
--> Processing Dependency: perl(Pod::Text) >= 3.15 for package: perl-Pod-Usage-1.63-3.el7.noarch
--> Processing Dependency: perl-Pod-Perldoc for package: perl-Pod-Usage-1.63-3.el7.noarch
---> Package perl-Text-ParseWords.noarch 0:3.29-4.el7 will be installed
--> Running transaction check
---> Package perl-Pod-Perldoc.noarch 0:3.20-4.el7 will be installed
--> Processing Dependency: perl(parent) for package: perl-Pod-Perldoc-3.20-4.el7.noarch
--> Processing Dependency: perl(HTTP::Tiny) for package: perl-Pod-Perldoc-3.20-4.el7.noarch
---> Package perl-podlators.noarch 0:2.5.1-3.el7 will be installed
--> Running transaction check
---> Package perl-HTTP-Tiny.noarch 0:0.033-3.el7 will be installed
---> Package perl-parent.noarch 1:0.225-244.el7 will be installed
--> Finished Dependency Resolution

Dependencies Resolved

================================================================================
 Package                 Arch    Version               Repository          Size
================================================================================
Installing:
 kernel-devel            x86_64  3.10.0-957.12.2.el7   C7.6.1810-updates   17 M
Installing for dependencies:
 perl                    x86_64  4:5.16.3-295.el7      base               8.0 M
 perl-Carp               noarch  1.26-244.el7          C7.0.1406-base      19 k
 perl-Encode             x86_64  2.51-7.el7            C7.0.1406-base     1.5 M
 perl-Exporter           noarch  5.68-3.el7            C7.0.1406-base      28 k
 perl-File-Path          noarch  2.09-2.el7            C7.0.1406-base      26 k
 perl-File-Temp          noarch  0.23.01-3.el7         C7.0.1406-base      56 k
 perl-Filter             x86_64  1.49-3.el7            C7.0.1406-base      76 k
 perl-Getopt-Long        noarch  2.40-3.el7            C7.5.1804-base      56 k
 perl-HTTP-Tiny          noarch  0.033-3.el7           C7.0.1406-base      38 k
 perl-PathTools          x86_64  3.40-5.el7            C7.0.1406-base      82 k
 perl-Pod-Escapes        noarch  1:1.04-295.el7        base                51 k
 perl-Pod-Perldoc        noarch  3.20-4.el7            C7.0.1406-base      87 k
 perl-Pod-Simple         noarch  1:3.28-4.el7          C7.0.1406-base     216 k
 perl-Pod-Usage          noarch  1.63-3.el7            C7.0.1406-base      27 k
 perl-Scalar-List-Utils  x86_64  1.27-248.el7          C7.0.1406-base      36 k
 perl-Socket             x86_64  2.010-5.el7           base                49 k
 perl-Storable           x86_64  2.45-3.el7            C7.0.1406-base      77 k
 perl-Text-ParseWords    noarch  3.29-4.el7            C7.0.1406-base      14 k
 perl-Time-HiRes         x86_64  4:1.9725-3.el7        C7.0.1406-base      45 k
 perl-Time-Local         noarch  1.2300-2.el7          C7.0.1406-base      24 k
 perl-constant           noarch  1.27-2.el7            C7.0.1406-base      19 k
 perl-libs               x86_64  4:5.16.3-295.el7      base               689 k
 perl-macros             x86_64  4:5.16.3-295.el7      base                44 k
 perl-parent             noarch  1:0.225-244.el7       C7.0.1406-base      12 k
 perl-podlators          noarch  2.5.1-3.el7           C7.0.1406-base     112 k
 perl-threads            x86_64  1.87-4.el7            C7.0.1406-base      49 k
 perl-threads-shared     x86_64  1.43-6.el7            C7.0.1406-base      39 k

Transaction Summary
================================================================================
Install  1 Package (+27 Dependent packages)

Total download size: 28 M
Installed size: 74 M
Downloading packages:
--------------------------------------------------------------------------------
Total                                              2.4 MB/s |  28 MB  00:11
Running transaction check
Running transaction test
Transaction test succeeded
Running transaction
  Installing : 1:perl-parent-0.225-244.el7.noarch                          1/28
  Installing : perl-HTTP-Tiny-0.033-3.el7.noarch                           2/28
  Installing : perl-podlators-2.5.1-3.el7.noarch                           3/28
  Installing : perl-Pod-Perldoc-3.20-4.el7.noarch                          4/28
  Installing : 1:perl-Pod-Escapes-1.04-295.el7.noarch                      5/28
  Installing : perl-Text-ParseWords-3.29-4.el7.noarch                      6/28
  Installing : perl-Encode-2.51-7.el7.x86_64                               7/28
  Installing : perl-Pod-Usage-1.63-3.el7.noarch                            8/28
  Installing : 4:perl-libs-5.16.3-295.el7.x86_64                           9/28
  Installing : 4:perl-macros-5.16.3-295.el7.x86_64                        10/28
  Installing : perl-Storable-2.45-3.el7.x86_64                            11/28
  Installing : perl-Exporter-5.68-3.el7.noarch                            12/28
  Installing : perl-constant-1.27-2.el7.noarch                            13/28
  Installing : perl-Socket-2.010-5.el7.x86_64                             14/28
  Installing : perl-Time-Local-1.2300-2.el7.noarch                        15/28
  Installing : perl-Carp-1.26-244.el7.noarch                              16/28
  Installing : 4:perl-Time-HiRes-1.9725-3.el7.x86_64                      17/28
  Installing : perl-PathTools-3.40-5.el7.x86_64                           18/28
  Installing : perl-Scalar-List-Utils-1.27-248.el7.x86_64                 19/28
  Installing : perl-File-Temp-0.23.01-3.el7.noarch                        20/28
  Installing : perl-File-Path-2.09-2.el7.noarch                           21/28
  Installing : perl-threads-shared-1.43-6.el7.x86_64                      22/28
  Installing : perl-threads-1.87-4.el7.x86_64                             23/28
  Installing : perl-Filter-1.49-3.el7.x86_64                              24/28
  Installing : 1:perl-Pod-Simple-3.28-4.el7.noarch                        25/28
  Installing : perl-Getopt-Long-2.40-3.el7.noarch                         26/28
  Installing : 4:perl-5.16.3-295.el7.x86_64                               27/28
  Installing : kernel-devel-3.10.0-957.12.2.el7.x86_64                    28/28
  Verifying  : perl-HTTP-Tiny-0.033-3.el7.noarch                           1/28
  Verifying  : perl-threads-shared-1.43-6.el7.x86_64                       2/28
  Verifying  : perl-Storable-2.45-3.el7.x86_64                             3/28
  Verifying  : 1:perl-Pod-Escapes-1.04-295.el7.noarch                      4/28
  Verifying  : perl-Exporter-5.68-3.el7.noarch                             5/28
  Verifying  : perl-constant-1.27-2.el7.noarch                             6/28
  Verifying  : perl-PathTools-3.40-5.el7.x86_64                            7/28
  Verifying  : perl-Socket-2.010-5.el7.x86_64                              8/28
  Verifying  : 1:perl-parent-0.225-244.el7.noarch                          9/28
  Verifying  : 4:perl-libs-5.16.3-295.el7.x86_64                          10/28
  Verifying  : perl-File-Temp-0.23.01-3.el7.noarch                        11/28
  Verifying  : 1:perl-Pod-Simple-3.28-4.el7.noarch                        12/28
  Verifying  : perl-Time-Local-1.2300-2.el7.noarch                        13/28
  Verifying  : 4:perl-macros-5.16.3-295.el7.x86_64                        14/28
  Verifying  : 4:perl-5.16.3-295.el7.x86_64                               15/28
  Verifying  : perl-Carp-1.26-244.el7.noarch                              16/28
  Verifying  : 4:perl-Time-HiRes-1.9725-3.el7.x86_64                      17/28
  Verifying  : perl-Scalar-List-Utils-1.27-248.el7.x86_64                 18/28
  Verifying  : perl-Pod-Usage-1.63-3.el7.noarch                           19/28
  Verifying  : kernel-devel-3.10.0-957.12.2.el7.x86_64                    20/28
  Verifying  : perl-Encode-2.51-7.el7.x86_64                              21/28
  Verifying  : perl-Pod-Perldoc-3.20-4.el7.noarch                         22/28
  Verifying  : perl-podlators-2.5.1-3.el7.noarch                          23/28
  Verifying  : perl-File-Path-2.09-2.el7.noarch                           24/28
  Verifying  : perl-threads-1.87-4.el7.x86_64                             25/28
  Verifying  : perl-Filter-1.49-3.el7.x86_64                              26/28
  Verifying  : perl-Getopt-Long-2.40-3.el7.noarch                         27/28
  Verifying  : perl-Text-ParseWords-3.29-4.el7.noarch                     28/28

Installed:
  kernel-devel.x86_64 0:3.10.0-957.12.2.el7

Dependency Installed:
  perl.x86_64 4:5.16.3-295.el7
  perl-Carp.noarch 0:1.26-244.el7
  perl-Encode.x86_64 0:2.51-7.el7
  perl-Exporter.noarch 0:5.68-3.el7
  perl-File-Path.noarch 0:2.09-2.el7
  perl-File-Temp.noarch 0:0.23.01-3.el7
  perl-Filter.x86_64 0:1.49-3.el7
  perl-Getopt-Long.noarch 0:2.40-3.el7
  perl-HTTP-Tiny.noarch 0:0.033-3.el7
  perl-PathTools.x86_64 0:3.40-5.el7
  perl-Pod-Escapes.noarch 1:1.04-295.el7
  perl-Pod-Perldoc.noarch 0:3.20-4.el7
  perl-Pod-Simple.noarch 1:3.28-4.el7
  perl-Pod-Usage.noarch 0:1.63-3.el7
  perl-Scalar-List-Utils.x86_64 0:1.27-248.el7
  perl-Socket.x86_64 0:2.010-5.el7
  perl-Storable.x86_64 0:2.45-3.el7
  perl-Text-ParseWords.noarch 0:3.29-4.el7
  perl-Time-HiRes.x86_64 4:1.9725-3.el7
  perl-Time-Local.noarch 0:1.2300-2.el7
  perl-constant.noarch 0:1.27-2.el7
  perl-libs.x86_64 4:5.16.3-295.el7
  perl-macros.x86_64 4:5.16.3-295.el7
  perl-parent.noarch 1:0.225-244.el7
  perl-podlators.noarch 0:2.5.1-3.el7
  perl-threads.x86_64 0:1.87-4.el7
  perl-threads-shared.x86_64 0:1.43-6.el7

Complete!
Loaded plugins: fastestmirror
Loading mirror speeds from cached hostfile
 * base: mirror.ams1.nl.leaseweb.net
 * extras: centos.mirror.transip.nl
 * updates: mirror.wd6.net
Package 4:perl-5.16.3-295.el7.x86_64 already installed and latest version
Package bzip2-1.0.6-13.el7.x86_64 already installed and latest version
Resolving Dependencies
--> Running transaction check
---> Package binutils.x86_64 0:2.27-34.base.el7 will be updated
---> Package binutils.x86_64 0:2.27-43.base.el7 will be an update
---> Package elfutils-libelf-devel.x86_64 0:0.176-4.el7 will be installed
--> Processing Dependency: elfutils-libelf(x86-64) = 0.176-4.el7 for package: elfutils-libelf-devel-0.176-4.el7.x86_64
--> Processing Dependency: pkgconfig(zlib) for package: elfutils-libelf-devel-0.176-4.el7.x86_64
---> Package gcc.x86_64 0:4.8.5-39.el7 will be installed
--> Processing Dependency: libgomp = 4.8.5-39.el7 for package: gcc-4.8.5-39.el7.x86_64
--> Processing Dependency: cpp = 4.8.5-39.el7 for package: gcc-4.8.5-39.el7.x86_64
--> Processing Dependency: libgcc >= 4.8.5-39.el7 for package: gcc-4.8.5-39.el7.x86_64
--> Processing Dependency: glibc-devel >= 2.2.90-12 for package: gcc-4.8.5-39.el7.x86_64
--> Processing Dependency: libmpfr.so.4()(64bit) for package: gcc-4.8.5-39.el7.x86_64
--> Processing Dependency: libmpc.so.3()(64bit) for package: gcc-4.8.5-39.el7.x86_64
---> Package make.x86_64 1:3.82-23.el7 will be updated
---> Package make.x86_64 1:3.82-24.el7 will be an update
--> Running transaction check
---> Package cpp.x86_64 0:4.8.5-39.el7 will be installed
---> Package elfutils-libelf.x86_64 0:0.172-2.el7 will be updated
--> Processing Dependency: elfutils-libelf(x86-64) = 0.172-2.el7 for package: elfutils-libs-0.172-2.el7.x86_64
---> Package elfutils-libelf.x86_64 0:0.176-4.el7 will be an update
---> Package glibc-devel.x86_64 0:2.17-307.el7.1 will be installed
--> Processing Dependency: glibc-headers = 2.17-307.el7.1 for package: glibc-devel-2.17-307.el7.1.x86_64
--> Processing Dependency: glibc = 2.17-307.el7.1 for package: glibc-devel-2.17-307.el7.1.x86_64
--> Processing Dependency: glibc-headers for package: glibc-devel-2.17-307.el7.1.x86_64
---> Package libgcc.x86_64 0:4.8.5-36.el7_6.2 will be updated
---> Package libgcc.x86_64 0:4.8.5-39.el7 will be an update
---> Package libgomp.x86_64 0:4.8.5-36.el7_6.2 will be updated
---> Package libgomp.x86_64 0:4.8.5-39.el7 will be an update
---> Package libmpc.x86_64 0:1.0.1-3.el7 will be installed
---> Package mpfr.x86_64 0:3.1.1-4.el7 will be installed
---> Package zlib-devel.x86_64 0:1.2.7-18.el7 will be installed
--> Running transaction check
---> Package elfutils-libs.x86_64 0:0.172-2.el7 will be updated
---> Package elfutils-libs.x86_64 0:0.176-4.el7 will be an update
---> Package glibc.x86_64 0:2.17-260.el7_6.5 will be updated
--> Processing Dependency: glibc = 2.17-260.el7_6.5 for package: glibc-common-2.17-260.el7_6.5.x86_64
---> Package glibc.x86_64 0:2.17-307.el7.1 will be an update
---> Package glibc-headers.x86_64 0:2.17-307.el7.1 will be installed
--> Processing Dependency: kernel-headers >= 2.2.1 for package: glibc-headers-2.17-307.el7.1.x86_64
--> Processing Dependency: kernel-headers for package: glibc-headers-2.17-307.el7.1.x86_64
--> Running transaction check
---> Package glibc-common.x86_64 0:2.17-260.el7_6.5 will be updated
---> Package glibc-common.x86_64 0:2.17-307.el7.1 will be an update
---> Package kernel-headers.x86_64 0:3.10.0-1127.el7 will be installed
--> Finished Dependency Resolution

Dependencies Resolved

================================================================================
 Package                    Arch        Version                 Repository
                                                                           Size
================================================================================
Installing:
 elfutils-libelf-devel      x86_64      0.176-4.el7             base       40 k
 gcc                        x86_64      4.8.5-39.el7            base       16 M
Updating:
 binutils                   x86_64      2.27-43.base.el7        base      5.9 M
 make                       x86_64      1:3.82-24.el7           base      421 k
Installing for dependencies:
 cpp                        x86_64      4.8.5-39.el7            base      5.9 M
 glibc-devel                x86_64      2.17-307.el7.1          base      1.1 M
 glibc-headers              x86_64      2.17-307.el7.1          base      689 k
 kernel-headers             x86_64      3.10.0-1127.el7         base      8.9 M
 libmpc                     x86_64      1.0.1-3.el7             base       51 k
 mpfr                       x86_64      3.1.1-4.el7             base      203 k
 zlib-devel                 x86_64      1.2.7-18.el7            base       50 k
Updating for dependencies:
 elfutils-libelf            x86_64      0.176-4.el7             base      195 k
 elfutils-libs              x86_64      0.176-4.el7             base      291 k
 glibc                      x86_64      2.17-307.el7.1          base      3.6 M
 glibc-common               x86_64      2.17-307.el7.1          base       11 M
 libgcc                     x86_64      4.8.5-39.el7            base      102 k
 libgomp                    x86_64      4.8.5-39.el7            base      158 k

Transaction Summary
================================================================================
Install  2 Packages (+7 Dependent packages)
Upgrade  2 Packages (+6 Dependent packages)

Total download size: 55 M
Downloading packages:
No Presto metadata available for base
--------------------------------------------------------------------------------
Total                                               19 MB/s |  55 MB  00:02
Running transaction check
Running transaction test
Transaction test succeeded
Running transaction
  Updating   : libgcc-4.8.5-39.el7.x86_64                                  1/25
  Updating   : glibc-2.17-307.el7.1.x86_64                                 2/25
warning: /etc/nsswitch.conf created as /etc/nsswitch.conf.rpmnew
  Updating   : glibc-common-2.17-307.el7.1.x86_64                          3/25
  Installing : mpfr-3.1.1-4.el7.x86_64                                     4/25
  Installing : libmpc-1.0.1-3.el7.x86_64                                   5/25
  Updating   : elfutils-libelf-0.176-4.el7.x86_64                          6/25
  Installing : cpp-4.8.5-39.el7.x86_64                                     7/25
  Updating   : libgomp-4.8.5-39.el7.x86_64                                 8/25
  Updating   : binutils-2.27-43.base.el7.x86_64                            9/25
  Installing : kernel-headers-3.10.0-1127.el7.x86_64                      10/25
  Installing : glibc-headers-2.17-307.el7.1.x86_64                        11/25
  Installing : glibc-devel-2.17-307.el7.1.x86_64                          12/25
  Installing : zlib-devel-1.2.7-18.el7.x86_64                             13/25
  Installing : elfutils-libelf-devel-0.176-4.el7.x86_64                   14/25
  Installing : gcc-4.8.5-39.el7.x86_64                                    15/25
  Updating   : elfutils-libs-0.176-4.el7.x86_64                           16/25
  Updating   : 1:make-3.82-24.el7.x86_64                                  17/25
  Cleanup    : elfutils-libs-0.172-2.el7.x86_64                           18/25
  Cleanup    : elfutils-libelf-0.172-2.el7.x86_64                         19/25
  Cleanup    : binutils-2.27-34.base.el7.x86_64                           20/25
  Cleanup    : 1:make-3.82-23.el7.x86_64                                  21/25
  Cleanup    : libgomp-4.8.5-36.el7_6.2.x86_64                            22/25
  Cleanup    : glibc-2.17-260.el7_6.5.x86_64                              23/25
  Cleanup    : glibc-common-2.17-260.el7_6.5.x86_64                       24/25
  Cleanup    : libgcc-4.8.5-36.el7_6.2.x86_64                             25/25
  Verifying  : gcc-4.8.5-39.el7.x86_64                                     1/25
  Verifying  : zlib-devel-1.2.7-18.el7.x86_64                              2/25
  Verifying  : glibc-common-2.17-307.el7.1.x86_64                          3/25
  Verifying  : libgomp-4.8.5-39.el7.x86_64                                 4/25
  Verifying  : 1:make-3.82-24.el7.x86_64                                   5/25
  Verifying  : kernel-headers-3.10.0-1127.el7.x86_64                       6/25
  Verifying  : glibc-2.17-307.el7.1.x86_64                                 7/25
  Verifying  : elfutils-libelf-0.176-4.el7.x86_64                          8/25
  Verifying  : libmpc-1.0.1-3.el7.x86_64                                   9/25
  Verifying  : elfutils-libs-0.176-4.el7.x86_64                           10/25
  Verifying  : glibc-headers-2.17-307.el7.1.x86_64                        11/25
  Verifying  : binutils-2.27-43.base.el7.x86_64                           12/25
  Verifying  : elfutils-libelf-devel-0.176-4.el7.x86_64                   13/25
  Verifying  : mpfr-3.1.1-4.el7.x86_64                                    14/25
  Verifying  : cpp-4.8.5-39.el7.x86_64                                    15/25
  Verifying  : glibc-devel-2.17-307.el7.1.x86_64                          16/25
  Verifying  : libgcc-4.8.5-39.el7.x86_64                                 17/25
  Verifying  : binutils-2.27-34.base.el7.x86_64                           18/25
  Verifying  : libgcc-4.8.5-36.el7_6.2.x86_64                             19/25
  Verifying  : glibc-common-2.17-260.el7_6.5.x86_64                       20/25
  Verifying  : glibc-2.17-260.el7_6.5.x86_64                              21/25
  Verifying  : libgomp-4.8.5-36.el7_6.2.x86_64                            22/25
  Verifying  : elfutils-libelf-0.172-2.el7.x86_64                         23/25
  Verifying  : 1:make-3.82-23.el7.x86_64                                  24/25
  Verifying  : elfutils-libs-0.172-2.el7.x86_64                           25/25

Installed:
  elfutils-libelf-devel.x86_64 0:0.176-4.el7      gcc.x86_64 0:4.8.5-39.el7

Dependency Installed:
  cpp.x86_64 0:4.8.5-39.el7             glibc-devel.x86_64 0:2.17-307.el7.1
  glibc-headers.x86_64 0:2.17-307.el7.1 kernel-headers.x86_64 0:3.10.0-1127.el7
  libmpc.x86_64 0:1.0.1-3.el7           mpfr.x86_64 0:3.1.1-4.el7
  zlib-devel.x86_64 0:1.2.7-18.el7

Updated:
  binutils.x86_64 0:2.27-43.base.el7          make.x86_64 1:3.82-24.el7

Dependency Updated:
  elfutils-libelf.x86_64 0:0.176-4.el7   elfutils-libs.x86_64 0:0.176-4.el7
  glibc.x86_64 0:2.17-307.el7.1          glibc-common.x86_64 0:2.17-307.el7.1
  libgcc.x86_64 0:4.8.5-39.el7           libgomp.x86_64 0:4.8.5-39.el7

Complete!
Copy iso file C:\Program Files\Oracle\VirtualBox\VBoxGuestAdditions.iso into the box /tmp/VBoxGuestAdditions.iso
Mounting Virtualbox Guest Additions ISO to: /mnt
mount: /dev/loop0 is write-protected, mounting read-only
Installing Virtualbox Guest Additions 6.1.6 - guest version is unknown
Verifying archive integrity... All good.
Uncompressing VirtualBox 6.1.6 Guest Additions for Linux........
VirtualBox Guest Additions installer
Copying additional installer modules ...
Installing additional modules ...
VirtualBox Guest Additions: Starting.
VirtualBox Guest Additions: Building the VirtualBox Guest Additions kernel
modules.  This may take a while.
VirtualBox Guest Additions: To build modules for other installed kernels, run
VirtualBox Guest Additions:   /sbin/rcvboxadd quicksetup <version>
VirtualBox Guest Additions: or
VirtualBox Guest Additions:   /sbin/rcvboxadd quicksetup all
VirtualBox Guest Additions: Building the modules for kernel
3.10.0-957.12.2.el7.x86_64.
Redirecting to /bin/systemctl start vboxadd.service
Redirecting to /bin/systemctl start vboxadd-service.service
Unmounting Virtualbox Guest Additions ISO from: /mnt
==> otuslinux: Checking for guest additions in VM...
==> otuslinux: Setting hostname...
==> otuslinux: Configuring and enabling network interfaces...
==> otuslinux: Rsyncing folder: /cygdrive/c/Users/preningav/Documents/GitHub/otus-linux/ => /vagrant
==> otuslinux: Running provisioner: shell...
    otuslinux: Running: inline script
    otuslinux: Loaded plugins: fastestmirror
    otuslinux: Loading mirror speeds from cached hostfile
    otuslinux:  * base: mirror.ams1.nl.leaseweb.net
    otuslinux:  * extras: centos.mirror.transip.nl
    otuslinux:  * updates: mirror.wd6.net
    otuslinux: Resolving Dependencies
    otuslinux: --> Running transaction check
    otuslinux: ---> Package gdisk.x86_64 0:0.8.10-3.el7 will be installed
    otuslinux: ---> Package hdparm.x86_64 0:9.43-5.el7 will be installed
    otuslinux: ---> Package mdadm.x86_64 0:4.1-4.el7 will be installed
    otuslinux: --> Processing Dependency: libreport-filesystem for package: mdadm-4.1-4.el7.x86_64
    otuslinux: ---> Package smartmontools.x86_64 1:7.0-2.el7 will be installed
    otuslinux: --> Processing Dependency: mailx for package: 1:smartmontools-7.0-2.el7.x86_64
    otuslinux: --> Running transaction check
    otuslinux: ---> Package libreport-filesystem.x86_64 0:2.1.11-53.el7.centos will be installed
    otuslinux: ---> Package mailx.x86_64 0:12.5-19.el7 will be installed
    otuslinux: --> Finished Dependency Resolution
    otuslinux:
    otuslinux: Dependencies Resolved
    otuslinux:
    otuslinux: ================================================================================
    otuslinux:  Package                  Arch       Version                     Repository
    otuslinux:                                                                            Size
    otuslinux: ================================================================================
    otuslinux: Installing:
    otuslinux:  gdisk                    x86_64     0.8.10-3.el7                base     190 k
    otuslinux:  hdparm                   x86_64     9.43-5.el7                  base      83 k
    otuslinux:  mdadm                    x86_64     4.1-4.el7                   base     439 k
    otuslinux:  smartmontools            x86_64     1:7.0-2.el7                 base     546 k
    otuslinux: Installing for dependencies:
    otuslinux:  libreport-filesystem     x86_64     2.1.11-53.el7.centos        base      41 k
    otuslinux:  mailx                    x86_64     12.5-19.el7                 base     245 k
    otuslinux:
    otuslinux: Transaction Summary
    otuslinux: ================================================================================
    otuslinux: Install  4 Packages (+2 Dependent packages)
    otuslinux:
    otuslinux: Total download size: 1.5 M
    otuslinux: Installed size: 4.3 M
    otuslinux: Downloading packages:
    otuslinux: --------------------------------------------------------------------------------
    otuslinux: Total                                              4.3 MB/s | 1.5 MB  00:00
    otuslinux: Running transaction check
    otuslinux: Running transaction test
    otuslinux: Transaction test succeeded
    otuslinux: Running transaction
    otuslinux:   Installing : libreport-filesystem-2.1.11-53.el7.centos.x86_64             1/6
    otuslinux:
    otuslinux:   Installing : mailx-12.5-19.el7.x86_64                                     2/6
    otuslinux:
    otuslinux:   Installing : 1:smartmontools-7.0-2.el7.x86_64                             3/6
    otuslinux:
    otuslinux:   Installing : mdadm-4.1-4.el7.x86_64                                       4/6
    otuslinux:
    otuslinux:   Installing : hdparm-9.43-5.el7.x86_64                                     5/6
    otuslinux:
    otuslinux:   Installing : gdisk-0.8.10-3.el7.x86_64                                    6/6
    otuslinux:
    otuslinux:   Verifying  : 1:smartmontools-7.0-2.el7.x86_64                             1/6
    otuslinux:
    otuslinux:   Verifying  : gdisk-0.8.10-3.el7.x86_64                                    2/6
    otuslinux:
    otuslinux:   Verifying  : mailx-12.5-19.el7.x86_64                                     3/6
    otuslinux:
    otuslinux:   Verifying  : hdparm-9.43-5.el7.x86_64                                     4/6
    otuslinux:
    otuslinux:   Verifying  : mdadm-4.1-4.el7.x86_64                                       5/6
    otuslinux:
    otuslinux:   Verifying  : libreport-filesystem-2.1.11-53.el7.centos.x86_64             6/6
    otuslinux:
    otuslinux:
    otuslinux: Installed:
    otuslinux:   gdisk.x86_64 0:0.8.10-3.el7          hdparm.x86_64 0:9.43-5.el7
    otuslinux:   mdadm.x86_64 0:4.1-4.el7             smartmontools.x86_64 1:7.0-2.el7
    otuslinux:
    otuslinux: Dependency Installed:
    otuslinux:   libreport-filesystem.x86_64 0:2.1.11-53.el7.centos mailx.x86_64 0:12.5-19.el7
    otuslinux:
    otuslinux: Complete!

C:\Users\...\Documents\GitHub\otus-linux>
```

заходим в виртуалку

```
C:\Users\preningav\Documents\GitHub\otus-linux>vagrant ssh
```

посмотрим какие блочные устройства у нас

[root@otuslinux vagrant]# fdisk -l

```
Disk /dev/sda: 42.9 GB, 42949672960 bytes, 83886080 sectors
Units = sectors of 1 * 512 = 512 bytes
Sector size (logical/physical): 512 bytes / 512 bytes
I/O size (minimum/optimal): 512 bytes / 512 bytes
Disk label type: dos
Disk identifier: 0x0009ef88

   Device Boot      Start         End      Blocks   Id  System
/dev/sda1   *        2048    83886079    41942016   83  Linux

Disk /dev/sdb: 1572 MB, 1572864000 bytes, 3072000 sectors
Units = sectors of 1 * 512 = 512 bytes
Sector size (logical/physical): 512 bytes / 512 bytes
I/O size (minimum/optimal): 512 bytes / 512 bytes


Disk /dev/sdc: 1572 MB, 1572864000 bytes, 3072000 sectors
Units = sectors of 1 * 512 = 512 bytes
Sector size (logical/physical): 512 bytes / 512 bytes
I/O size (minimum/optimal): 512 bytes / 512 bytes


Disk /dev/sdd: 1572 MB, 1572864000 bytes, 3072000 sectors
Units = sectors of 1 * 512 = 512 bytes
Sector size (logical/physical): 512 bytes / 512 bytes
I/O size (minimum/optimal): 512 bytes / 512 bytes


Disk /dev/sde: 1572 MB, 1572864000 bytes, 3072000 sectors
Units = sectors of 1 * 512 = 512 bytes
Sector size (logical/physical): 512 bytes / 512 bytes
I/O size (minimum/optimal): 512 bytes / 512 bytes


Disk /dev/sdf: 1572 MB, 1572864000 bytes, 3072000 sectors
Units = sectors of 1 * 512 = 512 bytes
Sector size (logical/physical): 512 bytes / 512 bytes
I/O size (minimum/optimal): 512 bytes / 512 bytes
```





[root@otuslinux vagrant]# lsblk

```
NAME   MAJ:MIN RM  SIZE RO TYPE MOUNTPOINT
sda      8:0    0   40G  0 disk
└─sda1   8:1    0   40G  0 part /
sdb      8:16   0  1.5G  0 disk
sdc      8:32   0  1.5G  0 disk
sdd      8:48   0  1.5G  0 disk
sde      8:64   0  1.5G  0 disk
sdf      8:80   0  1.5G  0 disk
```




[root@otuslinux vagrant]# lshw

```
otuslinux
    description: Computer
    product: VirtualBox
    vendor: innotek GmbH
    version: 1.2
    serial: 0
    width: 64 bits
    capabilities: smbios-2.5 dmi-2.5 vsyscall32
    configuration: family=Virtual Machine uuid=E0D85DDA-5F5C-754A-AA6B-1C5FB590EC43
  *-core
       description: Motherboard
       product: VirtualBox
       vendor: Oracle Corporation
       physical id: 0
       version: 1.2
       serial: 0
     *-firmware
          description: BIOS
          vendor: innotek GmbH
          physical id: 0
          version: VirtualBox
          date: 12/01/2006
          size: 128KiB
          capacity: 128KiB
          capabilities: isa pci cdboot bootselect int9keyboard int10video acpi
     *-memory
          description: System memory
          physical id: 1
          size: 1GiB
     *-cpu
          product: Intel(R) Xeon(R) Gold 6130 CPU @ 2.10GHz
          vendor: Intel Corp.
          vendor_id: GenuineIntel
          physical id: 2
          bus info: cpu@0
          width: 64 bits
          capabilities: fpu fpu_exception wp vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ht syscall nx rdtscp x86-64 constant_tsc rep_good nopl xtopology nonstop_tsc eagerfpu pni pclmulqdq ssse3 cx16 pcid sse4_1 sse4_2 x2apic movbe popcnt aes xsave avx rdrand hypervisor lahf_lm abm 3dnowprefetch fsgsbase avx2 invpcid rdseed clflushopt arch_capabilities
     *-pci
          description: Host bridge
          product: 440FX - 82441FX PMC [Natoma]
          vendor: Intel Corporation
          physical id: 100
          bus info: pci@0000:00:00.0
          version: 02
          width: 32 bits
          clock: 33MHz
        *-isa
             description: ISA bridge
             product: 82371SB PIIX3 ISA [Natoma/Triton II]
             vendor: Intel Corporation
             physical id: 1
             bus info: pci@0000:00:01.0
             version: 00
             width: 32 bits
             clock: 33MHz
             capabilities: isa bus_master
             configuration: latency=0
        *-ide
             description: IDE interface
             product: 82371AB/EB/MB PIIX4 IDE
             vendor: Intel Corporation
             physical id: 1.1
             bus info: pci@0000:00:01.1
             logical name: scsi0
             version: 01
             width: 32 bits
             clock: 33MHz
             capabilities: ide isa_compatibility_mode_controller__supports_both_channels_switched_to_pci_native_mode__supports_bus_mastering bus_master emulated
             configuration: driver=ata_piix latency=64
             resources: irq:0 ioport:1f0(size=8) ioport:3f6 ioport:170(size=8) ioport:376 ioport:d000(size=16)
           *-disk
                description: ATA Disk
                product: VBOX HARDDISK
                vendor: VirtualBox
                physical id: 0.0.0
                bus info: scsi@0:0.0.0
                logical name: /dev/sda
                version: 1.0
                serial: VBcbdedc4c-2d61633b
                size: 40GiB (42GB)
                capabilities: partitioned partitioned:dos
                configuration: ansiversion=5 logicalsectorsize=512 sectorsize=512 signature=0009ef88
              *-volume
                   description: Linux filesystem partition
                   physical id: 1
                   bus info: scsi@0:0.0.0,1
                   logical name: /dev/sda1
                   logical name: /
                   capacity: 39GiB
                   capabilities: primary bootable
                   configuration: mount.fstype=xfs mount.options=rw,seclabel,relatime,attr2,inode64,noquota state=mounted
        *-display
             description: VGA compatible controller
             product: VirtualBox Graphics Adapter
             vendor: InnoTek Systemberatung GmbH
             physical id: 2
             bus info: pci@0000:00:02.0
             version: 00
             width: 32 bits
             clock: 33MHz
             capabilities: vga_controller rom
             configuration: driver=vboxvideo latency=0
             resources: irq:18 memory:e0000000-e0ffffff
        *-network:0
             description: Ethernet interface
             product: 82540EM Gigabit Ethernet Controller
             vendor: Intel Corporation
             physical id: 3
             bus info: pci@0000:00:03.0
             logical name: eth0
             version: 02
             serial: 52:54:00:8a:fe:e6
             size: 1Gbit/s
             capacity: 1Gbit/s
             width: 32 bits
             clock: 66MHz
             capabilities: pm pcix bus_master cap_list ethernet physical tp 10bt 10bt-fd 100bt 100bt-fd 1000bt-fd autonegotiation
             configuration: autonegotiation=on broadcast=yes driver=e1000 driverversion=7.3.21-k8-NAPI duplex=full ip=10.0.2.15 latency=64 link=yes mingnt=255 multicast=yes port=twisted pair speed=1Gbit/s
             resources: irq:19 memory:f0000000-f001ffff ioport:d010(size=8)
        *-generic
             description: System peripheral
             product: VirtualBox Guest Service
             vendor: InnoTek Systemberatung GmbH
             physical id: 4
             bus info: pci@0000:00:04.0
             version: 00
             width: 32 bits
             clock: 33MHz
             configuration: driver=vboxguest latency=0
             resources: irq:20 ioport:d020(size=32) memory:f0400000-f07fffff memory:f0800000-f0803fff
        *-multimedia
             description: Multimedia audio controller
             product: 82801AA AC'97 Audio Controller
             vendor: Intel Corporation
             physical id: 5
             bus info: pci@0000:00:05.0
             version: 01
             width: 32 bits
             clock: 33MHz
             capabilities: bus_master
             configuration: driver=snd_intel8x0 latency=64
             resources: irq:21 ioport:d100(size=256) ioport:d200(size=64)
        *-bridge
             description: Bridge
             product: 82371AB/EB/MB PIIX4 ACPI
             vendor: Intel Corporation
             physical id: 7
             bus info: pci@0000:00:07.0
             version: 08
             width: 32 bits
             clock: 33MHz
             capabilities: bridge
             configuration: driver=piix4_smbus latency=0
             resources: irq:9
        *-network:1
             description: Ethernet interface
             product: 82540EM Gigabit Ethernet Controller
             vendor: Intel Corporation
             physical id: 8
             bus info: pci@0000:00:08.0
             logical name: eth1
             version: 02
             serial: 08:00:27:71:1b:81
             size: 1Gbit/s
             capacity: 1Gbit/s
             width: 32 bits
             clock: 66MHz
             capabilities: pm pcix bus_master cap_list ethernet physical tp 10bt 10bt-fd 100bt 100bt-fd 1000bt-fd autonegotiation
             configuration: autonegotiation=on broadcast=yes driver=e1000 driverversion=7.3.21-k8-NAPI duplex=full ip=192.168.11.101 latency=64 link=yes mingnt=255 multicast=yes port=twisted pair speed=1Gbit/s
             resources: irq:16 memory:f0820000-f083ffff ioport:d240(size=8)
        *-sata
             description: SATA controller
             product: 82801HM/HEM (ICH8M/ICH8M-E) SATA Controller [AHCI mode]
             vendor: Intel Corporation
             physical id: d
             bus info: pci@0000:00:0d.0
             logical name: scsi3
             logical name: scsi4
             logical name: scsi5
             logical name: scsi6
             logical name: scsi7
             version: 02
             width: 32 bits
             clock: 33MHz
             capabilities: sata pm ahci_1.0 bus_master cap_list emulated
             configuration: driver=ahci latency=64
             resources: irq:21 ioport:d248(size=8) ioport:d250(size=4) ioport:d258(size=8) ioport:d260(size=4) ioport:d270(size=16) memory:f0840000-f0841fff
           *-disk:0
                description: ATA Disk
                product: VBOX HARDDISK
                vendor: VirtualBox
                physical id: 0
                bus info: scsi@3:0.0.0
                logical name: /dev/sdb
                version: 1.0
                serial: VBfb275e21-024eb0d3
                size: 1500MiB (1572MB)
                configuration: ansiversion=5 logicalsectorsize=512 sectorsize=512
           *-disk:1
                description: ATA Disk
                product: VBOX HARDDISK
                vendor: VirtualBox
                physical id: 1
                bus info: scsi@4:0.0.0
                logical name: /dev/sdc
                version: 1.0
                serial: VB91cfde2d-312dce68
                size: 1500MiB (1572MB)
                configuration: ansiversion=5 logicalsectorsize=512 sectorsize=512
           *-disk:2
                description: ATA Disk
                product: VBOX HARDDISK
                vendor: VirtualBox
                physical id: 2
                bus info: scsi@5:0.0.0
                logical name: /dev/sdd
                version: 1.0
                serial: VBf6de9b56-242757ad
                size: 1500MiB (1572MB)
                configuration: ansiversion=5 logicalsectorsize=512 sectorsize=512
           *-disk:3
                description: ATA Disk
                product: VBOX HARDDISK
                vendor: VirtualBox
                physical id: 3
                bus info: scsi@6:0.0.0
                logical name: /dev/sde
                version: 1.0
                serial: VB29d18ecd-32bebda6
                size: 1500MiB (1572MB)
                configuration: ansiversion=5 logicalsectorsize=512 sectorsize=512
           *-disk:4
                description: ATA Disk
                product: VBOX HARDDISK
                vendor: VirtualBox
                physical id: 0.0.0
                bus info: scsi@7:0.0.0
                logical name: /dev/sdf
                version: 1.0
                serial: VB0397e425-a5c91a44
                size: 1500MiB (1572MB)
                configuration: ansiversion=5 logicalsectorsize=512 sectorsize=512
     *-pnp00:00
          product: PnP device PNP0303
          physical id: 3
          capabilities: pnp
          configuration: driver=i8042 kbd
     *-pnp00:01
          product: PnP device PNP0f03
          physical id: 4
          capabilities: pnp
          configuration: driver=i8042 aux
```


и более кратко:

[root@otuslinux vagrant]# lshw -short | grep disk
```
/0/100/1.1/0.0.0    /dev/sda   disk        42GB VBOX HARDDISK
/0/100/d/0          /dev/sdb   disk        1572MB VBOX HARDDISK
/0/100/d/1          /dev/sdc   disk        1572MB VBOX HARDDISK
/0/100/d/2          /dev/sdd   disk        1572MB VBOX HARDDISK
/0/100/d/3          /dev/sde   disk        1572MB VBOX HARDDISK
/0/100/d/0.0.0      /dev/sdf   disk        1572MB VBOX HARDDISK
```



[root@otuslinux vagrant]# lsscsi
```
[0:0:0:0]    disk    ATA      VBOX HARDDISK    1.0   /dev/sda
[3:0:0:0]    disk    ATA      VBOX HARDDISK    1.0   /dev/sdb
[4:0:0:0]    disk    ATA      VBOX HARDDISK    1.0   /dev/sdc
[5:0:0:0]    disk    ATA      VBOX HARDDISK    1.0   /dev/sdd
[6:0:0:0]    disk    ATA      VBOX HARDDISK    1.0   /dev/sde
[7:0:0:0]    disk    ATA      VBOX HARDDISK    1.0   /dev/sdf
```



Занулим на всякий случай суперблоки:

[root@otuslinux vagrant]# mdadm --zero-superblock --force /dev/sd{b,c,d,e,f}
```
mdadm: Unrecognised md component device - /dev/sdb
mdadm: Unrecognised md component device - /dev/sdc
mdadm: Unrecognised md component device - /dev/sdd
mdadm: Unrecognised md component device - /dev/sde
mdadm: Unrecognised md component device - /dev/sdf
```




Создаем рейд 5 ( -l уровень рейда, -n (колличество устройств)

[root@otuslinux vagrant]# mdadm --create --verbose /dev/md0 -l 5 -n 5 /dev/sd{b,c,d,e,f}
```
mdadm: layout defaults to left-symmetric
mdadm: layout defaults to left-symmetric
mdadm: chunk size defaults to 512K
mdadm: size set to 1533952K
mdadm: Defaulting to version 1.2 metadata
mdadm: array /dev/md0 started.
```



Проверим что рейд собрался нормально

[root@otuslinux vagrant]# cat /proc/mdstat
```
Personalities : [raid6] [raid5] [raid4]
md0 : active raid5 sdf[5] sde[3] sdd[2] sdc[1] sdb[0]
      6135808 blocks super 1.2 level 5, 512k chunk, algorithm 2 [5/5] [UUUUU]

unused devices: <none>
```



[root@otuslinux vagrant]# mdadm -D /dev/md0
```
/dev/md0:
           Version : 1.2
     Creation Time : Sun May 10 10:08:55 2020
        Raid Level : raid5
        Array Size : 6135808 (5.85 GiB 6.28 GB)
     Used Dev Size : 1533952 (1498.00 MiB 1570.77 MB)
      Raid Devices : 5
     Total Devices : 5
       Persistence : Superblock is persistent

       Update Time : Sun May 10 10:09:36 2020
             State : clean
    Active Devices : 5
   Working Devices : 5
    Failed Devices : 0
     Spare Devices : 0

            Layout : left-symmetric
        Chunk Size : 512K

Consistency Policy : resync

              Name : otuslinux:0  (local to host otuslinux)
              UUID : 889e905e:64e5c754:d2ac4979:3f73a834
            Events : 18

    Number   Major   Minor   RaidDevice State
       0       8       16        0      active sync   /dev/sdb
       1       8       32        1      active sync   /dev/sdc
       2       8       48        2      active sync   /dev/sdd
       3       8       64        3      active sync   /dev/sde
       5       8       80        4      active sync   /dev/sdf
```


создадим  mdadm.conf чтобы ОС запомнила состояние рейда:

Сначала убедимся, что информация верна:

[root@otuslinux vagrant]# mdadm --detail --scan --verbose
```
ARRAY /dev/md0 level=raid5 num-devices=5 metadata=1.2 name=otuslinux:0 UUID=889e905e:64e5c754:d2ac4979:3f73a834
   devices=/dev/sdb,/dev/sdc,/dev/sdd,/dev/sde,/dev/sdf
```
   
   
а теперь создадим mdadm.conf
[root@otuslinux vagrant]#mkdir /etc/mdadm

[root@otuslinux vagrant]# echo "DEVICE partitions" > /etc/mdadm/mdadm.conf

[root@otuslinux mdadm]# mdadm --detail --scan --verbose | awk '/ARRAY/{print}' >> /etc/mdadm/mdadm.conf




Проверим после перезагрузки:

[root@otuslinux mdadm]# shutdown -r
Shutdown scheduled for Sun 2020-05-10 08:43:34 UTC, use 'shutdown -c' to cancel.
[root@otuslinux mdadm]#
Broadcast message from root@otuslinux (Sun 2020-05-10 08:42:34 UTC):

The system is going down for reboot at Sun 2020-05-10 08:43:34 UTC!

Connection to 127.0.0.1 closed by remote host.
Connection to 127.0.0.1 closed.

C:\Users\...\Documents\GitHub\otus-linux>vagrant ssh

[root@otuslinux vagrant]# mdadm --detail --scan --verbose
```
ARRAY /dev/md0 level=raid6 num-devices=5 metadata=1.2 name=otuslinux:0 UUID=d4f79884:71821689:cc439d4b:dfebab40
   devices=/dev/sdb,/dev/sdc,/dev/sdd,/dev/sde,/dev/sdf
```
   
[root@otuslinux vagrant]# cat /proc/mdstat
```
Personalities : [raid6] [raid5] [raid4]
md0 : active raid5 sdf[5] sde[3] sdd[2] sdc[1] sdb[0]
      6135808 blocks super 1.2 level 5, 512k chunk, algorithm 2 [5/5] [UUUUU]
```



Работает, сломаем рейд.

[root@otuslinux vagrant]# mdadm /dev/md0 --fail /dev/sde
```
mdadm: set /dev/sde faulty in /dev/md0
```



[root@otuslinux vagrant]# cat /proc/mdstat
```
Personalities : [raid6] [raid5] [raid4]
md0 : active raid5 sdf[5] sde[3](F) sdd[2] sdc[1] sdb[0]
      6135808 blocks super 1.2 level 5, 512k chunk, algorithm 2 [5/4] [UUU_U]

unused devices: <none>
```



[root@otuslinux vagrant]# mdadm -D /dev/md0
```
/dev/md0:
           Version : 1.2
     Creation Time : Sun May 10 10:08:55 2020
        Raid Level : raid5
        Array Size : 6135808 (5.85 GiB 6.28 GB)
     Used Dev Size : 1533952 (1498.00 MiB 1570.77 MB)
      Raid Devices : 5
     Total Devices : 5
       Persistence : Superblock is persistent

       Update Time : Sun May 10 12:42:41 2020
             State : clean, degraded
    Active Devices : 4
   Working Devices : 4
    Failed Devices : 1
     Spare Devices : 0

            Layout : left-symmetric
        Chunk Size : 512K

Consistency Policy : resync

              Name : otuslinux:0  (local to host otuslinux)
              UUID : 889e905e:64e5c754:d2ac4979:3f73a834
            Events : 20

    Number   Major   Minor   RaidDevice State
       0       8       16        0      active sync   /dev/sdb
       1       8       32        1      active sync   /dev/sdc
       2       8       48        2      active sync   /dev/sdd
       -       0        0        3      removed
       5       8       80        4      active sync   /dev/sdf

       3       8       64        -      faulty   /dev/sde
```

	   
	   
Удалим сломанный диск из рейда:

[root@otuslinux vagrant]# mdadm /dev/md0 --remove /dev/sde
```
mdadm: hot removed /dev/sde from /dev/md0
```



Теперь добавим новый диск на тоже место (перед этим физически конечно нужно его заменить)

[root@otuslinux vagrant]# mdadm /dev/md0 --add /dev/sde
```
mdadm: added /dev/sde
```

Процесс ребилда видно командой:

[root@otuslinux vagrant]# mdadm /dev/md0 --add /dev/sde
```
mdadm: added /dev/sde
[root@otuslinux vagrant]# cat /proc/mdstat
Personalities : [raid6] [raid5] [raid4]
md0 : active raid5 sde[6] sdf[5] sdd[2] sdc[1] sdb[0]
      6135808 blocks super 1.2 level 5, 512k chunk, algorithm 2 [5/4] [UUU_U]
      [>....................]  recovery =  3.9% (60544/1533952) finish=0.4min speed=60544K/sec

unused devices: <none>
```

[root@otuslinux vagrant]# cat /proc/mdstat
```
Personalities : [raid6] [raid5] [raid4]
md0 : active raid5 sde[6] sdf[5] sdd[2] sdc[1] sdb[0]
      6135808 blocks super 1.2 level 5, 512k chunk, algorithm 2 [5/4] [UUU_U]
      [===>.................]  recovery = 15.6% (240384/1533952) finish=0.4min speed=48076K/sec

unused devices: <none>
```

[root@otuslinux vagrant]# cat /proc/mdstat
```
Personalities : [raid6] [raid5] [raid4]
md0 : active raid5 sde[6] sdf[5] sdd[2] sdc[1] sdb[0]
      6135808 blocks super 1.2 level 5, 512k chunk, algorithm 2 [5/5] [UUUUU]

unused devices: <none>
```



[root@otuslinux vagrant]# mdadm -D /dev/md0
```
/dev/md0:
           Version : 1.2
     Creation Time : Sun May 10 10:08:55 2020
        Raid Level : raid5
        Array Size : 6135808 (5.85 GiB 6.28 GB)
     Used Dev Size : 1533952 (1498.00 MiB 1570.77 MB)
      Raid Devices : 5
     Total Devices : 5
       Persistence : Superblock is persistent

       Update Time : Sun May 10 12:47:21 2020
             State : clean
    Active Devices : 5
   Working Devices : 5
    Failed Devices : 0
     Spare Devices : 0

            Layout : left-symmetric
        Chunk Size : 512K

Consistency Policy : resync

              Name : otuslinux:0  (local to host otuslinux)
              UUID : 889e905e:64e5c754:d2ac4979:3f73a834
            Events : 40

    Number   Major   Minor   RaidDevice State
       0       8       16        0      active sync   /dev/sdb
       1       8       32        1      active sync   /dev/sdc
       2       8       48        2      active sync   /dev/sdd
       6       8       64        3      active sync   /dev/sde
       5       8       80        4      active sync   /dev/sdf
```
	   
	   
	   
Создаем раздел GPT на RAID:

[root@otuslinux vagrant]# parted -s /dev/md0 mklabel gpt

Создаем партиции:

[root@otuslinux vagrant]# parted /dev/md0 mkpart primary ext4 0% 20%
```
Information: You may need to update /etc/fstab.
```

[root@otuslinux vagrant]# parted /dev/md0 mkpart primary ext4 20% 40%
```
Information: You may need to update /etc/fstab.
```

[root@otuslinux vagrant]# parted /dev/md0 mkpart primary ext4 40% 60%
```
Information: You may need to update /etc/fstab.
```

[root@otuslinux vagrant]# parted /dev/md0 mkpart primary ext4 60% 80%
```
Information: You may need to update /etc/fstab.
```

[root@otuslinux vagrant]# parted /dev/md0 mkpart primary ext4 80% 100%
```
Information: You may need to update /etc/fstab.
```


Создадим ФС

[root@otuslinux vagrant]# for i in $(seq 1 5); do mkfs.ext4 /dev/md0p$i; done
```
mke2fs 1.42.9 (28-Dec-2013)
Filesystem label=
OS type: Linux
Block size=4096 (log=2)
Fragment size=4096 (log=2)
Stride=128 blocks, Stripe width=512 blocks
76640 inodes, 306176 blocks
15308 blocks (5.00%) reserved for the super user
First data block=0
Maximum filesystem blocks=314572800
10 block groups
32768 blocks per group, 32768 fragments per group
7664 inodes per group
Superblock backups stored on blocks:
        32768, 98304, 163840, 229376, 294912

Allocating group tables: done
Writing inode tables: done
Creating journal (8192 blocks): done
Writing superblocks and filesystem accounting information: done

mke2fs 1.42.9 (28-Dec-2013)
Filesystem label=
OS type: Linux
Block size=4096 (log=2)
Fragment size=4096 (log=2)
Stride=128 blocks, Stripe width=512 blocks
76800 inodes, 306688 blocks
15334 blocks (5.00%) reserved for the super user
First data block=0
Maximum filesystem blocks=314572800
10 block groups
32768 blocks per group, 32768 fragments per group
7680 inodes per group
Superblock backups stored on blocks:
        32768, 98304, 163840, 229376, 294912

Allocating group tables: done
Writing inode tables: done
Creating journal (8192 blocks): done
Writing superblocks and filesystem accounting information: done

mke2fs 1.42.9 (28-Dec-2013)
Filesystem label=
OS type: Linux
Block size=4096 (log=2)
Fragment size=4096 (log=2)
Stride=128 blocks, Stripe width=512 blocks
76800 inodes, 307200 blocks
15360 blocks (5.00%) reserved for the super user
First data block=0
Maximum filesystem blocks=314572800
10 block groups
32768 blocks per group, 32768 fragments per group
7680 inodes per group
Superblock backups stored on blocks:
        32768, 98304, 163840, 229376, 294912

Allocating group tables: done
Writing inode tables: done
Creating journal (8192 blocks): done
Writing superblocks and filesystem accounting information: done

mke2fs 1.42.9 (28-Dec-2013)
Filesystem label=
OS type: Linux
Block size=4096 (log=2)
Fragment size=4096 (log=2)
Stride=128 blocks, Stripe width=512 blocks
76800 inodes, 306688 blocks
15334 blocks (5.00%) reserved for the super user
First data block=0
Maximum filesystem blocks=314572800
10 block groups
32768 blocks per group, 32768 fragments per group
7680 inodes per group
Superblock backups stored on blocks:
        32768, 98304, 163840, 229376, 294912

Allocating group tables: done
Writing inode tables: done
Creating journal (8192 blocks): done
Writing superblocks and filesystem accounting information: done

mke2fs 1.42.9 (28-Dec-2013)
Filesystem label=
OS type: Linux
Block size=4096 (log=2)
Fragment size=4096 (log=2)
Stride=128 blocks, Stripe width=512 blocks
76640 inodes, 306176 blocks
15308 blocks (5.00%) reserved for the super user
First data block=0
Maximum filesystem blocks=314572800
10 block groups
32768 blocks per group, 32768 fragments per group
7664 inodes per group
Superblock backups stored on blocks:
        32768, 98304, 163840, 229376, 294912

Allocating group tables: done
Writing inode tables: done
Creating journal (8192 blocks): done
Writing superblocks and filesystem accounting information: done
```




И смонтируем

[root@otuslinux vagrant]# mkdir -p /raid/part{1,2,3,4,5}


[root@otuslinux vagrant]# for i in $(seq 1 5); do mount /dev/md0p$i /raid/part$i; done

Обновим /etc/fstab  добавив информацию для монтирования

[root@otuslinux vagrant]# echo "#RAID DEVICE" >> /etc/fstab
[root@otuslinux vagrant]# for i in $(seq 1 5); do echo `sudo blkid /dev/md0p$i | awk '{print $2}'` /u0$i ext4 defaults 0 0 >> /etc/fstab; done




Добавим в vagrantfile строчки по автоподнятию рейда:

после строчки:   yum install -y mdadm smartmontools hdparm gdisk mc
добавим
```
mdadm --zero-superblock --force /dev/sd{b,c,d,e,f}
          mdadm --create --verbose --force /dev/md0 -l 5 -n 5 /dev/sd{b,c,d,e,f}
          mkdir /etc/mdadm
          echo "DEVICE partitions" > /etc/mdadm/mdadm.conf
          mdadm --detail --scan --verbose | awk '/ARRAY/ {print}' >> /etc/mdadm/mdadm.conf
          parted -s /dev/md0 mklabel gpt
          parted /dev/md0 mkpart primary ext4 0% 20%
          parted /dev/md0 mkpart primary ext4 20% 40%
          parted /dev/md0 mkpart primary ext4 40% 60%
          parted /dev/md0 mkpart primary ext4 60% 80%
          parted /dev/md0 mkpart primary ext4 80% 100%
          for i in $(seq 1 5); do mkfs.ext4 /dev/md0p$i; done
          mkdir -p /raid/part{1,2,3,4,5}
          for i in $(seq 1 5); do mount /dev/md0p$i /raid/part$i; done
          echo "#RAID DEVICE" >> /etc/fstab
          for i in $(seq 1 5); do echo `sudo blkid /dev/md0p$i | awk '{print $2}'` /u0$i ext4 defaults 0 0 >> /etc/fstab; done
```

ДЗ вернули с ошибкой:

Здравствуйте, стенд поднимается, массив собирается. После перезагрузки стенда вот такая картина:

[root@otuslinux ~]# lsblk
```
NAME      MAJ:MIN RM  SIZE RO TYPE  MOUNTPOINT
sda         8:0    0   40G  0 disk
└─sda1      8:1    0   40G  0 part  /
sdb         8:16   0  1.5G  0 disk
└─md0       9:0    0  5.9G  0 raid5
  ├─md0p1 259:0    0  1.2G  0 md    /raid/part1
  ├─md0p2 259:1    0  1.2G  0 md    /raid/part2
  ├─md0p3 259:2    0  1.2G  0 md    /raid/part3
  ├─md0p4 259:3    0  1.2G  0 md    /raid/part4
  └─md0p5 259:4    0  1.2G  0 md    /raid/part5
sdc         8:32   0  1.5G  0 disk
└─md0       9:0    0  5.9G  0 raid5
  ├─md0p1 259:0    0  1.2G  0 md    /raid/part1
  ├─md0p2 259:1    0  1.2G  0 md    /raid/part2
  ├─md0p3 259:2    0  1.2G  0 md    /raid/part3
  ├─md0p4 259:3    0  1.2G  0 md    /raid/part4
  └─md0p5 259:4    0  1.2G  0 md    /raid/part5
sdd         8:48   0  1.5G  0 disk
└─md0       9:0    0  5.9G  0 raid5
  ├─md0p1 259:0    0  1.2G  0 md    /raid/part1
  ├─md0p2 259:1    0  1.2G  0 md    /raid/part2
  ├─md0p3 259:2    0  1.2G  0 md    /raid/part3
  ├─md0p4 259:3    0  1.2G  0 md    /raid/part4
  └─md0p5 259:4    0  1.2G  0 md    /raid/part5
sde         8:64   0  1.5G  0 disk
└─md0       9:0    0  5.9G  0 raid5
  ├─md0p1 259:0    0  1.2G  0 md    /raid/part1
  ├─md0p2 259:1    0  1.2G  0 md    /raid/part2
  ├─md0p3 259:2    0  1.2G  0 md    /raid/part3
  ├─md0p4 259:3    0  1.2G  0 md    /raid/part4
  └─md0p5 259:4    0  1.2G  0 md    /raid/part5
sdf         8:80   0  1.5G  0 disk
└─md0       9:0    0  5.9G  0 raid5
  ├─md0p1 259:0    0  1.2G  0 md    /raid/part1
  ├─md0p2 259:1    0  1.2G  0 md    /raid/part2
  ├─md0p3 259:2    0  1.2G  0 md    /raid/part3
  ├─md0p4 259:3    0  1.2G  0 md    /raid/part4
  └─md0p5 259:4    0  1.2G  0 md    /raid/part5
```

[vagrant@otuslinux ~]$ sudo -i
[root@otuslinux ~]# reboot now
```
Connection to 127.0.0.1 closed by remote host.
Connection to 127.0.0.1 closed.
shaad@shaad-mobile:~/Teach/otus-linux$ vssh
Last login: Mon May 11 13:47:24 2020 from 10.0.2.2
```

[root@otuslinux ~]# lsblk
```
NAME      MAJ:MIN RM  SIZE RO TYPE  MOUNTPOINT
sda         8:0    0   40G  0 disk
└─sda1      8:1    0   40G  0 part  /
sdb         8:16   0  1.5G  0 disk
└─md0       9:0    0  5.9G  0 raid5
  ├─md0p1 259:0    0  1.2G  0 md    /u01
  ├─md0p2 259:1    0  1.2G  0 md    /u02
  ├─md0p3 259:2    0  1.2G  0 md    /u03
  ├─md0p4 259:3    0  1.2G  0 md    /u04
  └─md0p5 259:4    0  1.2G  0 md    /u05
sdc         8:32   0  1.5G  0 disk
└─md0       9:0    0  5.9G  0 raid5
  ├─md0p1 259:0    0  1.2G  0 md    /u01
  ├─md0p2 259:1    0  1.2G  0 md    /u02
  ├─md0p3 259:2    0  1.2G  0 md    /u03
  ├─md0p4 259:3    0  1.2G  0 md    /u04
  └─md0p5 259:4    0  1.2G  0 md    /u05
sdd         8:48   0  1.5G  0 disk
└─md0       9:0    0  5.9G  0 raid5
  ├─md0p1 259:0    0  1.2G  0 md    /u01
  ├─md0p2 259:1    0  1.2G  0 md    /u02
  ├─md0p3 259:2    0  1.2G  0 md    /u03
  ├─md0p4 259:3    0  1.2G  0 md    /u04
  └─md0p5 259:4    0  1.2G  0 md    /u05
sde         8:64   0  1.5G  0 disk
└─md0       9:0    0  5.9G  0 raid5
  ├─md0p1 259:0    0  1.2G  0 md    /u01
  ├─md0p2 259:1    0  1.2G  0 md    /u02
  ├─md0p3 259:2    0  1.2G  0 md    /u03
  ├─md0p4 259:3    0  1.2G  0 md    /u04
  └─md0p5 259:4    0  1.2G  0 md    /u05
sdf         8:80   0  1.5G  0 disk
└─md0       9:0    0  5.9G  0 raid5
  ├─md0p1 259:0    0  1.2G  0 md    /u01
  ├─md0p2 259:1    0  1.2G  0 md    /u02
  ├─md0p3 259:2    0  1.2G  0 md    /u03
  ├─md0p4 259:3    0  1.2G  0 md    /u04
  └─md0p5 259:4    0  1.2G  0 md    /u05
```


Исправил в vagrantfile строчку: for i in $(seq 1 5); do echo `sudo blkid /dev/md0p$i | awk '{print $2}'` /raid/part$i ext4 defaults 0 0 >> /etc/fstab; done

теперь после ребута тоже так:

[root@otuslinux ~]# lsblk
```
NAME      MAJ:MIN RM  SIZE RO TYPE  MOUNTPOINT
sda         8:0    0   40G  0 disk
└─sda1      8:1    0   40G  0 part  /
sdb         8:16   0  1.5G  0 disk
└─md0       9:0    0  5.9G  0 raid5
  ├─md0p1 259:0    0  1.2G  0 md    /raid/part1
  ├─md0p2 259:1    0  1.2G  0 md    /raid/part2
  ├─md0p3 259:2    0  1.2G  0 md    /raid/part3
  ├─md0p4 259:3    0  1.2G  0 md    /raid/part4
  └─md0p5 259:4    0  1.2G  0 md    /raid/part5
sdc         8:32   0  1.5G  0 disk
└─md0       9:0    0  5.9G  0 raid5
  ├─md0p1 259:0    0  1.2G  0 md    /raid/part1
  ├─md0p2 259:1    0  1.2G  0 md    /raid/part2
  ├─md0p3 259:2    0  1.2G  0 md    /raid/part3
  ├─md0p4 259:3    0  1.2G  0 md    /raid/part4
  └─md0p5 259:4    0  1.2G  0 md    /raid/part5
sdd         8:48   0  1.5G  0 disk
└─md0       9:0    0  5.9G  0 raid5
  ├─md0p1 259:0    0  1.2G  0 md    /raid/part1
  ├─md0p2 259:1    0  1.2G  0 md    /raid/part2
  ├─md0p3 259:2    0  1.2G  0 md    /raid/part3
  ├─md0p4 259:3    0  1.2G  0 md    /raid/part4
  └─md0p5 259:4    0  1.2G  0 md    /raid/part5
sde         8:64   0  1.5G  0 disk
└─md0       9:0    0  5.9G  0 raid5
  ├─md0p1 259:0    0  1.2G  0 md    /raid/part1
  ├─md0p2 259:1    0  1.2G  0 md    /raid/part2
  ├─md0p3 259:2    0  1.2G  0 md    /raid/part3
  ├─md0p4 259:3    0  1.2G  0 md    /raid/part4
  └─md0p5 259:4    0  1.2G  0 md    /raid/part5
sdf         8:80   0  1.5G  0 disk
└─md0       9:0    0  5.9G  0 raid5
  ├─md0p1 259:0    0  1.2G  0 md    /raid/part1
  ├─md0p2 259:1    0  1.2G  0 md    /raid/part2
  ├─md0p3 259:2    0  1.2G  0 md    /raid/part3
  ├─md0p4 259:3    0  1.2G  0 md    /raid/part4
  └─md0p5 259:4    0  1.2G  0 md    /raid/part5
```









