FROM node:10-slim

LABEL version="0.0.1"
LABEL repository="https://github.com/scentregroup/github-actions"
LABEL homepage="https://github.com/scentregroup/github-actions/danger-js"
LABEL maintainer="Scott Talbot <stalbot@scentregroup.com>"

LABEL com.github.actions.name="Danger"
LABEL com.github.actions.description="Runs danger-js."
LABEL com.github.actions.icon="shield"
LABEL com.github.actions.color="green"

COPY "package.json" "/usr/local/package.json"
COPY "package-lock.json" "/usr/local/package-lock.json"
RUN npm -g ci
RUN ln -s /usr/local/node_modules/.bin/danger /usr/local/bin/danger

ENTRYPOINT ["/usr/local/bin/danger"]
CMD ["ci"]
