FROM tendermint/tendermint:0.22.3
LABEL maintainer "dev@bigchaindb.com"
WORKDIR /
USER root
RUN apk --update add bash
COPY genesis.json.template /etc/tendermint/genesis.json
COPY tendermint_entrypoint.bash /
VOLUME /tendermint /tendermint_node_data
EXPOSE 26656 26657
ENTRYPOINT ["/tendermint_entrypoint.bash"]
