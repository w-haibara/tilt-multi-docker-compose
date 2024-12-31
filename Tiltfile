# -*- mode: Python -*-

version_settings(constraint='>=0.33.21')

# Extentions
load('ext://git_resource', 'git_checkout')

# App1
app1_dir = './repos/app1'
git_checkout('git@github.com:w-haibara/tilt-sample-app-1.git', app1_dir)

docker_compose(app1_dir + '/docker-compose.yml')

docker_build(
  'sample/app1',
  app1_dir,
  live_update = [
    sync(app1_dir, '/app'),

    restart_container()
  ])

dc_resource('app1', labels=["api"])
