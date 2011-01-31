desc "Deploy"
task :deploy => :"deploy:live"

namespace :deploy do
  # desc "Deploy to Dev"
  # task :dev => :build do
    # rsync "$HOME/Sites/photos.tritarget.org"
  # end
  
  desc "Deploy to Live"
  task :live do
    rsync "ktohg@tritarget.org:photos.tritarget.org"
  end
  
  # desc "Deploy to Dev and Live"
  # task :all => [:dev, :live]
  
  def rsync(location)
    sh "rsync -rtz --delete _site/ #{location}/"
  end
end
