FROM ubuntu:16.04
WORKDIR /mydirtydeeds
RUN apt-get update && apt-get install -y curl
COPY epico-curler.sh .
CMD ["./epico-curler.sh"]