# -*- mode: Python -*-

# Importing required Tilt modules
# from tilt.dev import helm_chart
docker_build('datree/admission-webhook', '.', dockerfile='./Dockerfile')

k8s_yaml(helm('./charts/datree-admission-webhook/', name='admission-webhook', values='./values.yaml'))


# Define the path to your Helm chart
chart_path = '/Users/nivweiss/Documents/datree/admission-webhook-datree/charts/datree-admission-webhook/'
values_file = './values.yaml'

# Define the Tilt configuration
# Use the `helm_chart` function to create a Helm chart deployment in Tilt
# helm_chart(chart_path, values=[values_file])

# Optionally, you can specify additional Tilt configurations for your project, such as sync rules, port forwarding, etc.

# Example sync rule to watch for changes in your Helm chart
# sync.sync(chart_path)

# Example port forwarding rule to access services within the cluster
# k8s_port_forward('service-name', local_port=8080, remote_port=80)

# You can add more Tilt configurations based on your project requirements

# Save this Tiltfile and run 'tilt up' to start Tilt and deploy your custom Helm chart.