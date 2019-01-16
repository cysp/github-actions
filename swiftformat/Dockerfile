FROM swift:4.2.1

LABEL version="0.0.1"
LABEL repository="https://github.com/scentregroup/github-actions"
LABEL homepage="https://github.com/scentregroup/github-actions"
LABEL maintainer="Scott Talbot <stalbot@scentregroup.com>"

LABEL com.github.actions.name="SwiftFormat"
LABEL com.github.actions.description="Runs SwiftFormat in linting mode."
LABEL com.github.actions.icon="check"
LABEL com.github.actions.color="orange"

RUN mkdir -p /opt/github-action-swiftformat
RUN git clone https://github.com/nicklockwood/SwiftFormat.git -b 0.37.2 --single-branch --depth 1 /opt/github-action-swiftformat
RUN (cd /opt/github-action-swiftformat; swift build -c release)
RUN (cd /usr/local/bin; ln -s /opt/github-action-swiftformat/.build/release/swiftformat)

ENTRYPOINT ["/usr/local/bin/swiftformat"]
CMD ["--lint", "."]
