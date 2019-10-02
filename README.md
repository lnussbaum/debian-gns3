# Debian 9 and Debian 10 image for GNS3

Simple script to create a QEMU Debian image using debootstrap and nbd, suitable for use as a GNS3 appliance.

Run with: ETH_DEVICE=no ./qemu-debian-create-image stretch3.qcow2 debian9 stretch

Or for Debian 10:
ETH_DEVICE=no ./qemu-debian-create-image debian10.qcow2 debian10 buster

 * Initially automated from <http://diogogomes.com/2012/07/13/debootstrap-kvm-image/> by Kamil Trzcinski <http://ayufan.eu>
 * Later modified to <https://gist.github.com/spectra/10301941>
 * And then <https://gist.github.com/jalsot/a24aa543021889ad0c70>
 * And then <https://gist.github.com/ldhieu/716db2f79ce49b95aa18e29885c16259>

## TODO

* port_name_format is wrong

# To publish

zip debian9-0.1.qcow2.zip debian9-0.1.qcow2

rsync -avzP debian9-0.1.qcow2.zip lucas@paradis.debian.org:public_html/gns3/
