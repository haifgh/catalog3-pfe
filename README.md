Building a simple LAMP stack and deploying Application using Ansible Playbooks.
-------------------------------------------

These playbooks require Ansible 1.2.

These playbooks are meant to be a reference and starter's guide to building
Ansible Playbooks. These playbooks were tested on Ubuntu 16.04 so we recommend
that you use Ubuntu to test these modules.

## 3-Tier Infrastructure

This 3-Tier Infrastructure stack can be on a single node or multiple nodes. The inventory file
`hosts` defines the nodes in which the stacks should be configured.

        [webservers]
        localhost

        [dbservers]
        localhost

For demo purpose we have configured this system to run on localhost server but we can allways change server name in hosts file to configure it on multiple servers.

Here the webserver would be configured on the local host and the dbserver also on local server. 
The stack can be deployed using the following command:

        ansible-playbook -i hosts site.yml

Once done, you can check the results by browsing to http://localhost/index.php.
You should see a simple test page and a list of databases retrieved from the
database server.

## Next Steps

We can allways improve this playbook to execute some of the additional installations and below mentioned future steps can be taken:

 - As of now this covers ubuntu only so we can extend this to other operating system also.
 - We can use multiple servers instead of localhost server to extend this architecture to multiple servers.
 - We can include a fully working application instead of sample ping application for a complete setup.
 - We can include other development tools also to this playbook.
 - When Ansible combines with Docker then which is a best combination for efficient software product
 -  
