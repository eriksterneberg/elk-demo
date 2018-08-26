# elk-demo
This repo is a demo of how to use Filebeat to send service logs to ELK.

## Usage
In a terminal window, type:
`$ docker-compose up`

Wait a minute or two, then go to `http://localhost:5601/` in your browser.
Kibana will ask you to configure your first index. Type "filebeat*" and click 'Next step', then choose @timestamp as
the Time Filter field name and finally 'Create index pattern'.

Then choose 'Discover' from the menu, and voila! You should see one log that was collected
from the 'web' service.

## Troubleshooting
* If Elasticsearch doesn't start, please configure at least 4 GB of memory to your containers.
