

# Rioxx v3.0 DSpace Integration

The official documentation on how to configure the Rioxx v3.0 endpoint is available at [Lyrasis: Rioxx v3 schema compliance](https://wiki.lyrasis.org/display/DSDOC8x/Rioxx+v3+schema+compliance).
This repository keeps the patch file to be installed on DSpace 7 (REST backend) to enable/configure the Rioxx v3.0 OAI feature.


## How to install the patch file
1. First move to the branch you want to install the patch on i.e. `git checkout <my-dspace-branch>`
2. Then run the following command `git apply <path-of-patch-file>`
3. Once the patch is applied you will need to add all the newly added/modified files to git with `git add *`
4. Then commit the patch changes with `git commit -m 'Installed Rioxx patch for DSpace 7.6.1'`
5. Push the changes to your remote


## Additional SOLR core configuration
Once the patch for DSpace 7 has been installed, there is minimal configuration needed in SOLR. The OAI core schema.xml needs to be updated on the SOLR service in order to allow the indexing of a couple of new fields that have been added. See changes to schema.xml (dspace/solr/oai/conf) once the patch has been applied.

## Branch for the Rioxx integration

[DSpace 7.6.1 - REST](https://github.com/cambridge-collection/DSpace/tree/dspace-7.6.1-rioxx) 
