# OSX Limitations

There are some limitations in `networking` for `Docker fo mac` so we can not utilize full functionality of `--net="host"` command on top of that we are exporting some of the most common ports from container to the host machine

**Common ports exposed**
80, 443, 3000, 3306, 3307, 3308, 8000, 8001, 8002, 8080, 9000

# Networking 

Due to the restrictions related with the OSX networking. We are not able to expose the network from container to host with our `--net=host` argument.

The workaround for that is the possiblity to expose specific `ports` in the default `--net=bridge` option. 


# Multipele terminal usage

If you will use our plain method calls in many terminal windows you will end up with an error similiar to this:

> docker: Error response from daemon: driver failed programming external connectivity on endpoint nervous_rosalind (8f5ce6fe3a15980607eec2532f0e421a37878b58c0d35f7de545d67dcce873fd): Bind for 0.0.0.0:9000 failed: port is already allocated.

This is because each of our call is exposing all of our `Common ports`. This is done for simplicy. But if you know which exact ports you need you can force to use only the with `DB_EXPOSE_PORTS` environment variable.

```
DB_EXPOSE_PORTS=80 npm server-start
> Listening for connections on port: 80
```
