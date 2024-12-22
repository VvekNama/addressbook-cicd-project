FROM tomcat:9.0-jdk11

# Remove the default ROOT application (optional)
RUN rm -rf /usr/local/tomcat/webapps/ROOT

# Copy your .war file to the webapps directory
COPY addressbook.war /usr/local/tomcat/webapps/ROOT.war

# Expose Tomcat's default port
EXPOSE 8080

# Start Tomcat
CMD ["catalina.sh", "run"]

