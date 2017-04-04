Week 4 Code

# Difference compared to Week3
## Frontend:
1. Added estimated value in detail.jade
2. Modified router.js to handle estiamted value used in detail.jade

## Backend:
1. Modify getDetailsByZpid API to call predict_server for predicted value

## Machine Learning
1. trainer - train a linear regression model (you can specify the csv file as argument)
2. predict_server - serve the trained model through RPC
3. ml_common - common definitions and methods shared by trainer and predict_server
4. ml_scheduler - bash script to automatically export mongodb and trigger the trainer

# NOTE:
1. Please replace all cloud amqp url with your own;
2. Please replace ZWS_ID with your own;
3. test.csv (under top level dir) can be used for your test;
4. docker image for Jupyter with Tensorflow: 
	docker run -d -p 8888:8888 jupyter/tensorflow-notebook
5. Jupyter Notebook file: jupyter_demo.py can be used for your test;
6. (Optional) ml_scheduler can be linked to cron job:
	help link: https://www.howtoforge.com/a-short-introduction-to-cron-jobs