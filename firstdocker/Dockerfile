FROM ubuntu:16.04

WORKDIR /mydir
RUN apt-get update && \
    apt-get install -y curl python
RUN curl -L https://yt-dl.org/downloads/latest/youtube-dl -o /usr/local/bin/youtube-dl
RUN chmod a+x /usr/local/bin/youtube-dl
ENV LC_ALL=C.UTF-8
ENTRYPOINT ["/usr/local/bin/youtube-dl"]

# NOTE from cource material
# ENTRYPOINT vs CMD can be confusing - in a properly set up image such as our youtube-dl 
# the command represents an argument list for the entrypoint. By default entrypoint is 
# set as /bin/sh and this is passed if no entrypoint is set. This is why giving path to 
# a script file as CMD works: you’re giving the file as a parameter to /bin/sh.

# In addition there are two ways to set them: exec form and shell form. We’ve been using 
# the exec form where the command itself is executed. In shell form the command that is 
# executed is wrapped with /bin/sh -c - it’s useful when you need to evaluate environment 
# variables in the command like $MYSQL_PASSWORD or similar.