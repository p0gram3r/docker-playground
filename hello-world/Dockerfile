FROM busybox

ENV TARGET_DIR="/bin"

COPY greet.sh ${TARGET_DIR}/greet
COPY farewell.sh ${TARGET_DIR}/farewell

RUN chmod +x ${TARGET_DIR}/greet
RUN chmod +x ${TARGET_DIR}/farewell

ENTRYPOINT ["greet"]
