# Python

```
python3 -m venv venv
pip freeze >requirements.txt para poner las depedendencias
pip install -r requirements.txt
```

To install from UCLV

```
pip install [package] -i https://nexus.uclv.edu.cu/repository/pypi/
```

From UCI http://nexus.prod.uci.cu/repository/pypi-all/

## Start postgres daemon

```
sudo systemctl start postgresql
```

# Docker

## Start

```bash
sudo dockerd
```

##Docker image pull from uclv

```
sudo docker pull docker.uclv.cu/{package}
```

### docker mongo create container

```
DB_NAME={NAME}
sudo docker run -d -p 27020:27017 --name $DB_NAME -e MONGO_INITDB_ROOT_USERNAME=$DB_NAME -e MONGO_INITDB_ROOT_PASSWORD=$DB_NAME docker.uclv.cu/{imageName}
```

# Run dynamo db

```
java -Djava.library.path=./DynamoDBLocal_lib -jar DynamoDBLocal.jar -sharedDb
```

# npm

## npm install from UCLV proxy uclv

```bash
npm install {package} --regstry=http://nexus.uclv.edu.cu/repository/npm
```

## create react app

```bash
npm_config_registry=http://nexus.uclv.edu.cu/repository/npm npx create-react-app {projectName}
```

# Postgres

## log in postgres user

```bash
su
su -l postgres
```

### linea de comando de postgres

```
psql {DATABASENAME}
```

# GPG

### Test gpg key

```
echo "test" | gpg --clearsign
```
