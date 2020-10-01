FROM quay.io/narendev/android-sdk:29

# this is the current stable verison , reference taken from https://flutter.dev/docs/development/tools/sdk/releases?tab=windows#stable-channel
ENV flutter_version=1.22.0

ENV FLUTTER_HOME=${HOME}/sdks/flutter \
    FLUTTER_VERSION=$flutter_version
ENV FLUTTER_ROOT=$FLUTTER_HOME

ENV PATH ${PATH}:${FLUTTER_HOME}/bin:${FLUTTER_HOME}/bin/cache/dart-sdk/bin

RUN git clone --branch ${FLUTTER_VERSION} https://github.com/flutter/flutter.git ${FLUTTER_HOME}

RUN yes | flutter doctor --android-licenses && flutter doctor