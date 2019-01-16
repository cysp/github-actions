FROM swift:4.2.1

LABEL version="0.0.1"
LABEL repository="https://github.com/scentregroup/github-actions"
LABEL homepage="https://github.com/scentregroup/github-actions"
LABEL maintainer="Scott Talbot <stalbot@scentregroup.com>"

LABEL com.github.actions.name="SwiftLint"
LABEL com.github.actions.description="Runs swiftlint."
LABEL com.github.actions.icon="check"
LABEL com.github.actions.color="orange"

RUN mkdir -p /opt/github-action-swiftlint
RUN git clone https://github.com/realm/SwiftLint.git -b 0.29.3 --single-branch --depth 1 /opt/github-action-swiftlint
RUN (cd /opt/github-action-swiftlint; make install)

ENTRYPOINT ["/usr/local/bin/swiftlint"]
CMD ["lint"]
