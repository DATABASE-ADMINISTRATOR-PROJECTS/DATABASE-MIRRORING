# DATABASE-MIRRORING
Database Mirroring is the process of creating the exact copy of your database in another server in real time. The Link below shows the full practical on how to configure Datbase Mirroring
https://youtu.be/Ql2ML6LYzg0
## DATABASE MIRRORING

It contains two database which is. 

- Principal
- Mirrored

Things to know about mirroring. 

- All data in the principal database automatically reflected in the mirrored database.
- Changes are instant.
- It has Automatic Failover (If there is a ***Witness server***)
    - Functions of a witness server
    - The witness server is responsible for detecting the failure of the principal server.
    - When the principal server fails, the witness server informs the mirrored server that it should take over as the new principal server.
    - This allows for automatic failover in the event of a principal server failure.
    - The witness server can also be used to monitor the status of the principal and mirrored servers to ensure that the mirrored server is up to date with the principal server.

## Steps for database mirroring

## Steps for database mirroring

*Database mirroring by default listen on port 5022*

*Ensure backups are not currently running for the database (It could mess up the synchronisation) *

1. Create a full backup of the principal database and restore it on the mirror server with `NO RECOVERY` option.
2. Take a transaction log backup on the principal server and restore it on the mirror server with `NO RECOVERY` option.
3. Configure database mirroring on the principal server.
4. Configure database mirroring on the mirror server.
5. Start the mirroring session on the principal server by connecting to the mirror server.
6. Start the mirroring session on the mirror server by connecting to the principal server.
7. Test the mirroring configuration by manually failing over to the mirror server.
8. Monitor the mirroring status using system views and performance counters.

 Click on the link and watch how it is done.

 https://youtu.be/Ql2ML6LYzg0
   
``![Mirroring](https://github.com/DATABASE-ADMINISTRATOR-PROJECTS/DATABASE-MIRRORING/assets/100750844/c17d1646-6696-4a8f-b32c-95fe40fe5e3f)



