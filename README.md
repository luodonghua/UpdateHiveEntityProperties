# UpdateHiveEntityProperties
Supporting Code for the HCC Blog posting describing Hive Entity Property Updates

# Example Requirements:
* Python 2.7+
* python packages: requests and json
* Accessible HTTP connection to your Atlas server through port 21000

# Configuring Example

You will need to specify the following property values within the Python script file 'UpdateAtlasEntity.py'

| Python Script property value | Default Value | Description |
|------------------------------|---------------|-------------|
| ATLAS_DOMAIN                 | server1       | The FQDN address for your Atlas Metadata Server.  If not certain, check in Ambari Atlas Summary |
| ATLAS_PORT                   | 21000         | This property should not require any changes unless the Atlas default port was changed during installation.  If you can access the Atlas UI from the same machine which will run the REST command, then you should be set to run this example program." |
| updateProperty               | description   | Can be any valid Atlas Entity property. The 'description' property will allow you to set the description for a data entity asset to a value of your choosing.|
| newValue                     | changeMe      | The new value for the property. |
| tableFQDN                    | default.drivers@HDP | The full hive table name you wish to search for.  The default value is the value will need to get changed to refelct one of your own tables using the format of '{database name}.{table Name}@{Cluster name}.  In my default example, I am extracting the entity for the default database, and a Hive table named 'drivers' located in a cluster named 'HDP'. |

# Running the example:

The supplied example will search for a single table meeting the search criteria specified with the property tableFQDN on the cluster specified by the properties defined above.  
  
After the properties have been updated, you will be ready to run the script.  To run the script from the command prompt, type 'python UpdateAtlasEntity.py'.
 
 
