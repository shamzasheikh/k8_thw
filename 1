#!/bin/bash
############################ Create ansibe hosts file ##############################

hostip=(`cat group_vars/HDP_Variables.yml |grep hostip|cut -d: -f2|tr -d \"|tr -d " "|tr ',' ' '`)
HOSTNAMES=(`cat group_vars/HDP_Variables.yml |grep HOSTNAMES|cut -d: -f2|tr -d \"|tr -d " "|tr ',' ' '`)

cm_host=(`cat group_vars/HDP_Variables.yml |grep AMBARI_SERVER|cut -d: -f2|tr -d \"|tr -d " "|tr ',' ' '`)

all_hostuser=(`cat group_vars/HDP_Variables.yml |grep all_hostuser|cut -d: -f2|tr -d \"|tr -d " "|tr ',' ' '`)

#####################################################################################
file_name=hosts
if [ -e "$file_name" ]
then
   rm -rf hosts
fi
#####################################################################################

echo [scripts] >> hosts
echo '# Provide entry on which script file i.e variable file will run ,usally this is machine where ansible is running ' >> hosts
for (( j=0; j<${#HOSTNAMES[@]}; j++ ))
do
        if [ ${cm_host} == ${HOSTNAMES[$j]} ]; then
                echo ${hostip[$j]} ansible_ssh_user=$all_hostuser  >> hosts
        fi
done
echo "" >> hosts

#####################################################################################
echo [slaves] >> hosts
echo '#Specify slaves node for HDP i.e agent machines' >> hosts
for (( i=0; i<${#hostip[@]}; i++ ))
do
        echo ${hostip[$i]} ansible_ssh_user=$all_hostuser  >> hosts
done
echo "" >> hosts

####################################################################################

echo [masters] >> hosts
echo '#node on which Ambari server needs to be installed' >> hosts
for (( k=0; k<${#HOSTNAMES[@]}; k++ ))
do
        if [ ${cm_host} == ${HOSTNAMES[$k]} ]; then
                echo ${hostip[$k]} ansible_ssh_user=$all_hostuser  >> hosts
        fi
done


