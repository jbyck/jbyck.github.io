desc "Watch Assets, Comple Jekyll"
task :watch do
  
  pids = [
    spawn 'jekyll',
    spawn 'scss --watch assets:stylesheets',
    spawn 'coffee -b -w -o javascripts -c assets/*.coffee'
  ]
  
  trap 'INT' do
    Process.kill 'INT', *pids
    exit
  end
  
  loop { sleep(1) }
  
end