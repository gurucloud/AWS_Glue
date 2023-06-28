# AWS_Glue
Jupyter interactive sessions using AWS Glue
Jupyter interactive sessions using AWS Glue
	In the serverless Spark environment of AWS Glue, a new notebook interface called Interactive Sessions for Jupyter is available. Interactive sessions give Jupyter notebooks and Jupyter-based IDEs like Jupyter Lab, Microsoft Visual Studio Code, JetBrains PyCharm, and others an on-demand, highly-scalable, serverless Spark backend. Interactive sessions start in a matter of seconds and instantly stop computing when idle.
Interactive sessions give Jupyter notebooks and Jupyter-based IDEs like Jupyter Lab, Microsoft Visual Studio Code, JetBrains PyCharm, and others an on-demand, highly-scalable, serverless Spark backend. Interactive sessions start in a matter of seconds and immediately terminate computing when idle. 

•	No clusters to set up or maintain
•	There are no unused clusters to pay for.
•	There is no need for upfront setting.
•	There is no resource conflict for the same development environment.
•	Simple installation and use
•	The exact same platform and serverless Spark runtime as AWS Glue extract, transform, and load (ETL) workloads

 Python versions by Glue Version

Different Glue versions support different Python versions. The following table below is for your reference, which also includes the associated repository's branch for each glue version.

Glue Version	Python 2 Version	Python 3 Version	aws-glue-libs branch
0.9	2.7	Not supported	glue-0.9
1.0	2.7	3.6	glue-1.0
2.0	Not supported	3.7	glue-2.0
3.0	Not supported	3.7	glue-3.0
4.0	Not supported	3.10	master


You may refer to AWS Glue's official release notes for more information.
Starting interactive Jupyter sessions
Only a few terminal commands are required to easily install interactive sessions. You can launch interactive sessions right away after installation, whenever you decide to do so. The installation on Linux and starting Jupyter processes are covered in the parts that follow.

Prerequisites
The AWS Command Line Interface (AWS CLI) must be correctly installed, set up, and functioning for these instructions to work. Python 3.6 or later is also presumed to be installed. Making API calls to AWS Glue requires the AWS CLI. Visit Installing or updating the newest version of the AWS CLI for further details on how to install the AWS CLI.
Before installing the AWS glue. 
First, need to install any browser in the Ubuntu machine in Linux or localhost. Use the following command for installing the browser.

•	sudo apt install chromium-browser
•	chromium-browser

 These are the commands that were used for installing the chromium.

Follow these steps to install AWS Glue interactive sessions:
To install and upgrade Jupyter, Boto3, and AWS Glue interactive sessions via PyPi, open a terminal and enter the commands below. Instead of Jupyter, you can install Jupyter Lab.

•	pip3 install --user --upgrade jupyter boto3 aws-glue-sessions
  
Run the following commands to locate the package installation location and set up Jupyter to use the AWS Glue PySpark and AWS Glue Spark kernels:

•	SITE_PACKAGES=$(pip3 show aws-glue-sessions | grep Location | awk '{print $2}')
•	jupyter kernelspec install $SITE_PACKAGES/aws_glue_interactive_sessions_kernel/glue_pyspark
•	sudo jupyter kernelspec install $SITE_PACKAGES/aws_glue_interactive_sessions_kernel/glue_pyspark
   

Install the Jupyter in the Ubuntu machine:

•	sudo apt install jupyter

After install the Both of the AWS Glue PySpark and the AWS Glue Spark kernels should be listed in the output along with the standard Python3 kernel. It should resemble the following:

•	sudo jupyter kernelspec install $SITE_PACKAGES/aws_glue_interactive_sessions_kernel/glue_pyspark
•	sudo jupyter kernelspec install $SITE_PACKAGES/aws_glue_interactive_sessions_kernel/glue_spark

To validate your install, run the following command:   

•	jupyter kernelspec list

Include the Access Key in Ubuntu CLI:

•	export AWS_ACCESS_KEY_ID=<A*******************>
•	export AWS_SECRET_ACCESS_KEY= <dUV***********************>

Run the jupyter notebook    
•	jupyter notebook

Licensing
The libraries in this repository licensed under the Amazon Software License (the "License"). They may not be used except in compliance with the License, a copy of which is included here in the LICENSE file.
