# DaticalDB4Concourse
Datical DB integration for Concourse

You can see a short demonstration video of Concourse and Datical DB [here](https://www.datical.com/videos/pivotal-cloud-foundry-and-datical-database-release-automation/).

To integrate Datical DB in your existing Concourse installation:

1. Download datical_package.yml and credentials.yml to the machine where Fly is installed.
2. Edit the datical_package.yml and credentials.yml to reflect your environment. Specifically, update credentials.yml to reflect your credentials and the IP address of your Git location. Also, update datical_package.yml to reflect the IP address of your Datical Monitoring Console server. Look for the "curl" call to find it.
2. Issue the following command: `fly -t main set-pipeline -p datical -c datical_package.yml -l credentials.yml`
3. In the Concourse Web UI, unpause the new `datical` pipeline and select the `+` button to request a new release.

For support, questions, comments, and compliments, please contact as at support@datical.com and on Twitter [@Datical](https://twitter.com/Datical).
