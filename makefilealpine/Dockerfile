# Fetch and build example
FROM alpine:latest AS buildstage
LABEL stage=builder
RUN echo "buildstage"
ENV REFRESHED_AT 2020-27-04
# --no-cache to reduce size
# use apk add build-base?
RUN apk --no-cache add alpine-sdk
WORKDIR /home/myuser
RUN git clone https://github.com/fkwiatkowski/TemplateMakefile.git
RUN cd TemplateMakefile && . ./environment-x86 && make clean && make

# Exec example
FROM alpine:latest as execexample
RUN echo "execexample"
WORKDIR /home/myuser
COPY --from=buildstage /home/myuser/TemplateMakefile/out/x86/helloworld.exe .
CMD ["./helloworld.exe"]

