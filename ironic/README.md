Initial Ironic element:

This is the initial ironic element. Note that currently the Ironic
project / programis not in a functional state. In it's current form this
element is intended for development use only.

This element checks the connection string and if using mysql and 
localhost(127.0.0.1) it will create the database and run dbsync.

Required options can be provided via heat. For example:

    rabbit:
        host: 192.0.2.1 
    nova:
        db: mysql://ironic:ironic@127.0.0.1/ironic
    mysql:
        create-users:
            username: ironic
            database: ironic
            password: ironic
    postfix:
        mailhostname: ironic
        maildomain: novalocal
        delay_warning_time: 4h
    keystone:
        host: 192.0.2.1
    glance:
        host: 192.0.2.1