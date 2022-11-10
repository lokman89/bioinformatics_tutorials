# i-Trop cluster

## Architecture of the i-Trop cluster

The IRD Bioinformatic Cluster is composed of a pool of machines reachable through a single entry point. The connections to the internal machines are managed by a master node that tries to ensure that proper balancing is made across the available nodes at a given moment: bioinfo-master.ird.fr

The cluster is composed of:

- 1 master 
- 3 nas servers for a 127To data storage
- 32 nodes servers : 8 nodes with 12 cores, 2 nodes with 16 cores, 4 nodes with 20 cores, 11 with 24 cores, 1 with 40 cores with RAM from 48Go to 1To and a GPU serveur with 8 RTX 2080 graphical cards.

Here is the architecture:

![This is an image.](https://github.com/lokman89/bioinformatics_tutorials/blob/temp/schema_cluster_150221.png)

## Connect to the cluster via *ssh*

Open the terminal application and type the following command:

`ssh login@bioinfo-master.ird.fr`

with login: your cluster account


**First connection**:

Your password has to be changed at your first connection.

“Mot de passe UNIX (actuel)”: you are asked to type the password provided in the account creation email.

Then type your new password twice.

The session will be automatically closed.

You will need to open a new session with your new password.

## Explore the cluster

The list of nodes in the cluster:

`sinfo -N nodes`

## Choose a partition

*short* partition: short Jobs < 1 day  

*normal* partition: job of maximum 7 days

*long* partition: 7 days< jobs < 45 days

*highmem* partition: jobs with more memory needs

*supermem* partition: jobs with much more memory needs

*gpu* partition: need of analyses on GPU cores


#### Choose **node5** (*highmem* partition):
`srun -p highmemplus --nodelist=node5 --pty bash -i`

## Data location

All the data used in this training can be found in the *scratch* space of node5.

`ls /scratch/genesys_training/`

## Launching a program on the cluster

### List the program already installed on the cluster:

`module avail`

### Display the description of a particular software

`module whatis module_type/module_name/version`

with module_type: bioinfo or system with module_name: the name of the module.

For example : for the version 1.7 of the bioinformatic software samtools:

`module whatis bioinfo/samtools/1.7`

### Load a particular software version

`module load module_type/module_name/version`

with module_type: bioinfo or system with module_name: the name of the module.

For example : for the version 1.7 of the bioinformatic software samtools:

`module load bioinfo/samtools/1.7`

### Unload a particular software version

`module unload module_type/module_name/version`

with module_type: bioinfo or system with module_name: the name of the module.

For example : for the version 1.7 of the bioinformatic software samtools:

`module unload bioinfo/samtools/1.7`

### Display all the modules loaded

`module list`

### unload all the modules loaded

`module unload`

