#! /bin/bash

# This script is for molecular dynamics software: LAMMPS

# Defien job name. Here the job name is defined as "test", which means the input file is "test.in"
#SBATCH --job-name=test

# Define the partition to submit. The partition name can be obtained by command "sinfo"
#SBATCH --partition=E5-2640V4

# Define the number of nodes allocated.
#SBATCH --nodes=4

# Define the number of cores allocated per node.
#SBATCH --ntasks-per-node=20

# Define the error and output files.
#SBATCH --error=%j.err
#SBATCH --output=%j.out

# Define the PATH of your lammps program.
LMP_EXE="/opt/MD/lammps/bin/lammps-cpu-12Dec18"

# Define other args for lammps program.
ADD_ARGS="-sf omp"

# Do not change any lines unless you know what you are doing.

# Generate a MPI nodelist.
CURDIR=`pwd`
rm -rf $CURDIR/nodelist.$SLURM_JOB_ID
NODES=`scontrol show hostnames $SLURM_JOB_NODELIST`
for i in $NODES
do
	echo "$i:$SLURM_NTASKS_PER_NODE" >> $CURDIR/nodelist.$SLURM_JOB_ID
done
# End of generation.

# 通过MPI运行LAMMPS
mpirun -genv I_MPI_FABRICS=tcp -machinefile $CURDIR/nodelist.$SLURM_JOB_ID $LMP_EXE -in $SLURM_JOB_NAME.in -l $SLURM_JOB_NAME.log $ADD_ARGS > $SLURM_JOB_NAME.sta

# 运行完后清理nodelist
rm -rf $CURDIR/nodelist.$SLURM_JOB_ID
