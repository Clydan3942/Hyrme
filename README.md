# Hyrme
Optimism fnd

sui4j CI License Coverage Branches

Hildr
Hildr is an OP Stack rollup client written in the Java 20 with GraalVM native.

Follow the spec

Rust
Go
Build
Prerequisites
Install GraalVM latest version
Build jar
./gradlew build
Build native
# use graalvm native plugin
./gradlew nativeCompile

# use native-image directly
./gradlew buildBinary

# build static binary
./gradlew buildBinaryStatic
Javadoc
For the latest javadocs for the main branch, run ./gradlew javadoc and open the document under the hildr-node/build/docs/javadoc/index.html in your browser.

Testing
./gradlew test
Running
Next copy .env.default to .env

cd docker/
cp .env.default .env
In the .env file, modify the L1_RPC_URL field to contain a valid Ethereum RPC. For the Optimism and Base testnets, this must be a Goerli RPC URL. This RPC can either be from a local node, or a provider such as Alchemy or Infura.

By default, the NETWORK field in .env is optimism-goerli, however base-goerli is also supported.

Start the docker containers

docker compose up -d
The docker setup contains a Grafana dashboard. To view sync progress, you can check the dashboard at http://localhost:3000 with the username hildr and password passw0rd. Alternatively, you can view Hildr's logs by running docker logs hildr-node --follow
