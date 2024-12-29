# -*- mode: Python -*-

version_settings(constraint='>=0.33.21')

docker_compose('docker-compose.yml')

docker_build(
  'sample/app1',
  './app1',
  live_update = [
    sync('./app1', '/app'),

    restart_container()
  ])

dc_resource('app1', labels=["server"])
