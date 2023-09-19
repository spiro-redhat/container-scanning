https://access.redhat.com/documentation/en-us/red_hat_quay/3/html-single/vulnerability_reporting_with_clair_on_red_hat_quay/index#testing-clair-with-quay
Once postgres is created, 
Run this command in the pod: 
/bin/bash -c 'echo "CREATE EXTENSION IF NOT EXISTS \"uuid-ossp\"" | psql -d clair -U postgres' 

 
To do: Create a tekton task that will use this container: quay.io/spiro-redhat/clairctl and points to the `Route` pass the image in as a parameter. 



