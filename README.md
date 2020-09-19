# Troubleshooting


* `ImportError: numpy.core.multiarray failed to import`
> Downgrade numpy version to `1.18.0`




# Tips

* Kill all processes of which names include some `${proc_name}`
> `ps -ef | grep ${proc_name} | grep -v grep | awk '{print $2}' | xargs -r kill -9`
