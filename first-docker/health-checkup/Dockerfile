##########################################
# 05. Healthcheck Dockerfile
##########################################
FROM nginx:alphine
HEALTHCHECK --interval=30s --timeout=5s --start-period=5s CMD curl -f http:/localhost/ || exit 1
EXPOSE 80
CMD [ "nginx", "-g", "daemon off" ]