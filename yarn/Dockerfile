FROM alpine
RUN touch ~/.profile
RUN apk add --no-cache curl bash nodejs
RUN curl -o- -L https://yarnpkg.com/install.sh | bash
RUN echo $HOME
ENV PATH="root/.yarn/bin:/root/.config/yarn/global/node_modules/.bin:${PATH}"
RUN echo $PATH
RUN yarn -v
COPY entry-point.sh /bin
RUN chmod +x /bin/entry-point.sh
ENTRYPOINT ["/bin/entry-point.sh"]
CMD ["/bin/bash"]
