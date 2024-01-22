## Set up env variables

export DISTRO_PATH=/workspace/bahmni-docker-compose/bahmni-distro-sgs && \
export OPENMRS_CONFIG_PATH=$DISTRO_PATH/openmrs_config && \
export BAHMNI_CONFIG_PATH=$DISTRO_PATH/bahmni_config && \
export OPENMRS_MODULES_PATH=$DISTRO_PATH/openmrs_modules && \
export BAHMNI_APPS_PATH=$DISTRO_PATH/bahmni_emr/bahmniapps

## Package 
mvn clean package

## Run all services 
docker-compose -p sgs up -d

## Clean up 
docker-compose -p sgs down -v

