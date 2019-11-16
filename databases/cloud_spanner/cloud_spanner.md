# Cloud Spanner
Fully managed, scalable, relational database service for regional and global application data

[Full Docs here](https://cloud.google.com/spanner/)

## SQL, transactions, and strong consistency at scale

Relational database structure with non relational database horizontal scale. With consistency across rows, regions and continents.
* 99.999% uptime 
* Scalable arbitrarily (damn near infinite)


<table id="table-spanner">
    <thead>
        <tr>
        <th></th>
        <th>Cloud Spanner</th>
        <th>Traditional Relational</th>
        <th>Traditional Non-Relational</th>
        </tr>
    </thead>
    <tbody>
        <tr>
        <td>Schema</td>
        <td><i class="material-icons nocontent md-green notranslate">done</i>Yes</td>
        <td><i class="material-icons nocontent md-green notranslate">done</i>Yes</td>
        <td><i class="material-icons nocontent md-red notranslate">clear</i>No</td>
        </tr>
        <tr>
        <td>SQL</td>
        <td><i class="material-icons nocontent md-green notranslate">done</i>Yes</td>
        <td><i class="material-icons nocontent md-green notranslate">done</i>Yes</td>
        <td><i class="material-icons nocontent md-red notranslate">clear</i>No</td>
        </tr>
        <tr>
        <td>Consistency</td>
        <td><i class="material-icons nocontent md-green notranslate">done</i>Strong</td>
        <td><i class="material-icons nocontent md-green notranslate">done</i>Strong</td>
        <td><i class="material-icons nocontent md-red notranslate">clear</i>Eventual</td>
        </tr>
        <tr>
        <td>Availability</td>
        <td><i class="material-icons nocontent md-green notranslate">done</i>High</td>
        <td><i class="material-icons nocontent md-red notranslate">clear</i>Failover</td>
        <td><i class="material-icons nocontent md-green notranslate">done</i>High</td>
        </tr>
        <tr>
        <td>Scalability</td>
        <td><i class="material-icons nocontent md-green notranslate">done</i>Horizontal</td>
        <td><i class="material-icons nocontent md-red notranslate">clear</i>Vertical</td>
        <td><i class="material-icons nocontent md-green notranslate">done</i>Horizontal</td>
        </tr>
        <tr>
        <td>Replication</td>
        <td><i class="material-icons nocontent md-green notranslate">done</i>Automatic</td>
        <td><i class="material-icons nocontent md-yellow notranslate">autorenew</i>Configurable</td>
        <td><i class="material-icons nocontent md-yellow notranslate">autorenew</i>Configurable</td>
        </tr>
    </tbody>
    </table>

## Features
### Globally scalable
Scalable across rows, regions and continents 

### Relational Schematics 
Everything you would expect from a relational database—schemas, ACID transactions, and SQL queries (ANSI 2011).

### Multi-Language support
[Client libraries](https://cloud.google.com/spanner/docs/reference/libraries/) in C#, Go, Java, Node.js, PHP, Python, and Ruby. 

[JDBC driver](https://cloud.google.com/spanner/docs/partners/drivers) for connectivity with popular third-party tools.

### Transactional Consistency
Purpose-built for external, strong, global transactional consistency.

### Enterprise Grade Security
Data-layer encryption, IAM integration for access and controls, and audit logging.
