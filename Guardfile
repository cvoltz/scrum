directories %w(. fonts images)
ignore %r{^scrum/}

notification :libnotify, timeout: 5, transient: true, urgency: :normal
clearing :off

guard 'rake', :task => 'build' do
  watch(/\.(css|rst|cli)$/)
  watch(/fonts\/*$/)
  watch(/images\/*$/)
  watch('Rakefile')
end
