## How to build a docker image

You can build a docker image in A Unix-like operating system, You can also build it in Windows operating system.

In Unix-Like, Example:

```bash
$ cd path/dolphinscheduler
$ sh ./docker/build/hooks/build
```

In Windows, Example:

```bat
c:\dolphinscheduler>.\docker\build\hooks\build.bat
```

Please read `./docker/build/hooks/build` `./docker/build/hooks/build.bat` script files if you don't understand

## Environment Variables

The Dolphin Scheduler image uses several environment variables which are easy to miss. While none of the variables are required, they may significantly aid you in using the image.

**`DATABASE_TYPE`**

This environment variable sets the type for database. The default value is `postgresql`.

**Note**: You must be specify it when start a standalone dolphinscheduler server. Like `master-server`, `worker-server`, `api-server`, `alert-server`.

**`DATABASE_DRIVER`**

This environment variable sets the type for database. The default value is `org.postgresql.Driver`.

**Note**: You must be specify it when start a standalone dolphinscheduler server. Like `master-server`, `worker-server`, `api-server`, `alert-server`.

**`DATABASE_HOST`**

This environment variable sets the host for database. The default value is `127.0.0.1`.

**Note**: You must be specify it when start a standalone dolphinscheduler server. Like `master-server`, `worker-server`, `api-server`, `alert-server`.

**`DATABASE_PORT`**

This environment variable sets the port for database. The default value is `5432`.

**Note**: You must be specify it when start a standalone dolphinscheduler server. Like `master-server`, `worker-server`, `api-server`, `alert-server`. 

**`DATABASE_USERNAME`**

This environment variable sets the username for database. The default value is `root`.

**Note**: You must be specify it when start a standalone dolphinscheduler server. Like `master-server`, `worker-server`, `api-server`, `alert-server`.

**`DATABASE_PASSWORD`**

This environment variable sets the password for database. The default value is `root`.

**Note**: You must be specify it when start a standalone dolphinscheduler server. Like `master-server`, `worker-server`, `api-server`, `alert-server`.

**`DATABASE_DATABASE`**

This environment variable sets the database for database. The default value is `dolphinscheduler`.

**Note**: You must be specify it when start a standalone dolphinscheduler server. Like `master-server`, `worker-server`, `api-server`, `alert-server`.

**`DATABASE_PARAMS`**

This environment variable sets the database for database. The default value is `characterEncoding=utf8`.

**Note**: You must be specify it when start a standalone dolphinscheduler server. Like `master-server`, `worker-server`, `api-server`, `alert-server`.

**`DOLPHINSCHEDULER_ENV_PATH`**

This environment variable sets the runtime environment for task. The default value is `/opt/dolphinscheduler/conf/env/dolphinscheduler_env.sh`.

**`DOLPHINSCHEDULER_DATA_BASEDIR_PATH`**

User data directory path, self configuration, please make sure the directory exists and have read write permissions. The default value is `/tmp/dolphinscheduler`

**`ZOOKEEPER_QUORUM`**

This environment variable sets zookeeper quorum for `master-server` and `worker-serverr`. The default value is `127.0.0.1:2181`.

**Note**: You must be specify it when start a standalone dolphinscheduler server. Like `master-server`, `worker-server`.

**`MASTER_EXEC_THREADS`**

This environment variable sets exec thread num for `master-server`. The default value is `100`.

**`MASTER_EXEC_TASK_NUM`**

This environment variable sets exec task num for `master-server`. The default value is `20`.

**`MASTER_HEARTBEAT_INTERVAL`**

This environment variable sets heartbeat interval for `master-server`. The default value is `10`.

**`MASTER_TASK_COMMIT_RETRYTIMES`**

This environment variable sets task commit retry times for `master-server`. The default value is `5`.

**`MASTER_TASK_COMMIT_INTERVAL`**

This environment variable sets task commit interval for `master-server`. The default value is `1000`.

**`MASTER_MAX_CPULOAD_AVG`**

This environment variable sets max cpu load avg for `master-server`. The default value is `100`.

**`MASTER_RESERVED_MEMORY`**

This environment variable sets reserved memory for `master-server`. The default value is `0.1`.

**`MASTER_LISTEN_PORT`**

This environment variable sets port for `master-server`. The default value is `5678`.

**`WORKER_EXEC_THREADS`**

This environment variable sets exec thread num for `worker-server`. The default value is `100`.

**`WORKER_HEARTBEAT_INTERVAL`**

This environment variable sets heartbeat interval for `worker-server`. The default value is `10`.

**`WORKER_FETCH_TASK_NUM`**

This environment variable sets fetch task num for `worker-server`. The default value is `3`.

**`WORKER_MAX_CPULOAD_AVG`**

This environment variable sets max cpu load avg for `worker-server`. The default value is `100`.

**`WORKER_RESERVED_MEMORY`**

This environment variable sets reserved memory for `worker-server`. The default value is `0.1`.

**`WORKER_WEIGHT`**

This environment variable sets port for `worker-server`. The default value is `100`.

**`WORKER_LISTEN_PORT`**

This environment variable sets port for `worker-server`. The default value is `1234`.

**`WORKER_GROUP`**

This environment variable sets group for `worker-server`. The default value is `default`.

**`XLS_FILE_PATH`**

This environment variable sets xls file path for `alert-server`. The default value is `/tmp/xls`.

**`MAIL_SERVER_HOST`**

This environment variable sets mail server host for `alert-server`. The default value is empty.

**`MAIL_SERVER_PORT`**

This environment variable sets mail server port for `alert-server`. The default value is empty.

**`MAIL_SENDER`**

This environment variable sets mail sender for `alert-server`. The default value is empty.

**`MAIL_USER=`**

This environment variable sets mail user for `alert-server`. The default value is empty.

**`MAIL_PASSWD`**

This environment variable sets mail password for `alert-server`. The default value is empty.

**`MAIL_SMTP_STARTTLS_ENABLE`**

This environment variable sets SMTP tls for `alert-server`. The default value is `true`.

**`MAIL_SMTP_SSL_ENABLE`**

This environment variable sets SMTP ssl for `alert-server`. The default value is `false`.

**`MAIL_SMTP_SSL_TRUST`**

This environment variable sets SMTP ssl truest for `alert-server`. The default value is empty.

**`ENTERPRISE_WECHAT_ENABLE`**

This environment variable sets enterprise wechat enable for `alert-server`. The default value is `false`.

**`ENTERPRISE_WECHAT_CORP_ID`**

This environment variable sets enterprise wechat corp id for `alert-server`. The default value is empty.

**`ENTERPRISE_WECHAT_SECRET`**

This environment variable sets enterprise wechat secret for `alert-server`. The default value is empty.

**`ENTERPRISE_WECHAT_AGENT_ID`**

This environment variable sets enterprise wechat agent id for `alert-server`. The default value is empty.

**`ENTERPRISE_WECHAT_USERS`**

This environment variable sets enterprise wechat users for `alert-server`. The default value is empty.

**`FRONTEND_API_SERVER_HOST`**

This environment variable sets api server host for `frontend`. The default value is `127.0.0.1`.

**Note**: You must be specify it when start a standalone dolphinscheduler server. Like `api-server`.

**`FRONTEND_API_SERVER_PORT`**

This environment variable sets api server port for `frontend`. The default value is `123451`.

**Note**: You must be specify it when start a standalone dolphinscheduler server. Like `api-server`.

## Initialization scripts

If you would like to do additional initialization in an image derived from this one, add one or more environment variable under `/root/start-init-conf.sh`, and modify template files in `/opt/dolphinscheduler/conf/*.tpl`.

For example, to add an environment variable `API_SERVER_PORT` in `/root/start-init-conf.sh`:

```
export API_SERVER_PORT=5555
``` 

and to modify `/opt/dolphinscheduler/conf/application-api.properties.tpl` template file, add server port:
```
server.port=${API_SERVER_PORT}
```

`/root/start-init-conf.sh` will dynamically generate config file:

```sh
echo "generate app config"
ls ${DOLPHINSCHEDULER_HOME}/conf/ | grep ".tpl" | while read line; do
eval "cat << EOF
$(cat ${DOLPHINSCHEDULER_HOME}/conf/${line})
EOF
" > ${DOLPHINSCHEDULER_HOME}/conf/${line%.*}
done

echo "generate nginx config"
sed -i "s/FRONTEND_API_SERVER_HOST/${FRONTEND_API_SERVER_HOST}/g" /etc/nginx/conf.d/dolphinscheduler.conf
sed -i "s/FRONTEND_API_SERVER_PORT/${FRONTEND_API_SERVER_PORT}/g" /etc/nginx/conf.d/dolphinscheduler.conf
```
