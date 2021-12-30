FROM jenkins/jenkins:2.319.1-lts-alpine

COPY --chown=jenkins:jenkins plugins.txt /usr/share/jenkins/ref/plugins.txt
RUN jenkins-plugin-cli -f /usr/share/jenkins/ref/plugins.txt

# Copy any relevant init scripts to the image.
COPY --chown=jenkins:jenkins init_scripts/authorization_strategy.groovy \
    /usr/share/jenkins/ref/init.groovy.d/authorization_strategy.groovy
