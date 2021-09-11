FROM alpine
WORKDIR /workdir

RUN apk --no-cache add curl jq bash
RUN curl -L -O https://raw.githubusercontent.com/ChaoticWeg/discord.sh/master/discord.sh && chmod +x discord.sh

ENTRYPOINT [ "./discord.sh" ]
