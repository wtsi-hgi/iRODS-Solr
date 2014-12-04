iRODS-Solr
==========

Offload irods metadata querying to an apache solr instance

Stage 1 is a script to pull out all the metadata information and send it to solr for indexing.
Stage 2 is to use triggers in the iCat database to populate a metadata audit table which will be periodically polled with any changes to be sent to solr. Once the changes have been made, the table can be truncated.

We can always apply the scripts in phase1 if we need to re-index from scratch.
