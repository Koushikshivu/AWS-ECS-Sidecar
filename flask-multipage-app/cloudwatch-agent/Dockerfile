#Use the official Amazon CloudWatch Agent image as the base
FROM amazon/cloudwatch-agent

# Set the working directory in the container
WORKDIR /etc/cwagent

# Copy the CloudWatch Agent configuration file into the image
COPY ./cw-agent-config.json /etc/cwagentconfig
#COPY ./amazon-cloudwatch-agent.toml /etc/amazon-cloudwatch-agent.toml
# Specify the environment variable to use the baked-in configuration
ENV CW_CONFIG_CONTENT=file:/etc/cwagentconfig

# Set the default command
CMD ["amazon-cloudwatch-agent", "-config", "/etc/cwagentconfig"]
