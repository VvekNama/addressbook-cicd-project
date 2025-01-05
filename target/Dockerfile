# FROM tomcat:9.0-jdk11

# # Remove the default ROOT application (optional)
# RUN rm -rf /usr/local/tomcat/webapps/ROOT

# # Copy your .war file to the webapps directory
# COPY addressbook.war /usr/local/tomcat/webapps/ROOT.war

# # Expose Tomcat's default port
# EXPOSE 8080

# # Start Tomcat
# CMD ["catalina.sh", "run"]

# Use the official Tomcat base image with JDK 11
FROM tomcat:9.0-jdk11

# Set environment variables for Tomcat
ENV CATALINA_HOME /usr/local/tomcat
ENV DEPLOY_DIR ${CATALINA_HOME}/webapps

# Remove the default ROOT application
RUN rm -rf ${DEPLOY_DIR}/ROOT

# Copy your WAR file to the webapps directory and rename it to ROOT.war
COPY addressbook.war ${DEPLOY_DIR}/ROOT.war

# Expose the default Tomcat HTTP port
EXPOSE 8080

# Run Tomcat in the foreground
CMD ["catalina.sh", "run"]
