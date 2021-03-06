STACK_NAME = cf-templates
TEMPLATE = template.json
REGION = us-east-1

BUCKET_NAME = com.cuffney.cf-templates

validate:
	aws cloudformation validate-template \
		--template-body file://${TEMPLATE} \
		--region ${REGION}

create:
	aws cloudformation create-stack \
		--stack-name ${STACK_NAME} \
		--template-body file://${TEMPLATE} \
		--parameters \
			ParameterKey=BucketName,ParameterValue=${BUCKET_NAME} \
		--region ${REGION} 

update:
	aws cloudformation update-stack \
		--stack-name ${STACK_NAME} \
		--template-body file://${TEMPLATE} \
		--parameters \
			ParameterKey=BucketName,ParameterValue=${BUCKET_NAME} \
		--region ${REGION} 

delete:
	aws cloudformation delete-stack \
		--stack-name ${STACK_NAME} \
		--region ${REGION} 

deploy:
	aws cloudformation deploy \
		--stack-name ${STACK_NAME} \
		--template-file ./${TEMPLATE} \
		--no-fail-on-empty-changeset \
		--parameter-overrides \
			BucketName=${BUCKET_NAME} \
		--region ${REGION} 