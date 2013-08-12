ironic-element
==============

initial ironic element

This Disk-image-builder element is currently used for testing the
Ironic baremetal service.

It is intended to be launched from boot-stack the boot-stack vm. The
Heat template (ironic.yaml) is configured with defaults that enable it
to make use of some of the Boot-Stack services, such as RabbitMq.

For testing the Ironic element may be built with the mysql element.
The ORC/configure script will attempt to detect if mysql is a local 
service and if so, it will create a ironic database and run db-sync.
If the Ironic image is built with out a local mysql, you must create
the database and run db-sync before starting the ironic image.
