require 'jekyll'

DATE = Time.now.strftime("%Y-%m-%d")
TIME = Time.now.strftime("%H:%M:%S")
POST_DIR = '_links'

desc "Generate new link"
task :new_link do

  puts 'Please write the link title'.yellow
  @name = STDIN.gets.chomp
  @title = @name.downcase.strip.gsub(' ', '-')
  @file = "#{POST_DIR}/#{@title}.md"

  puts
  puts 'Please write the link URL'.yellow
  @url = STDIN.gets.chomp

  puts
  puts 'Please specify the icon (fab fa-medium, fab fa-github-square etc.)'.yellow
  @icon = STDIN.gets.chomp

  if File.exists?("#{file}")
    raise 'File already exists'.red
  else
    File.open(@file, 'a+') do |file|
      file << "---\n"
      file << "layout: post\n"
      file << "title: \"#{@name}\"\n"
      file << "date: #{DATE} #{TIME}\n"
      file << "link: \"#{@url}\"\n"
      file << "icon: \"#{@icon}\"\n"
      file << "---\n"
    end
  end
  puts
  puts 'All done!'.green
end

desc "Delete latest link"
task :delete_link do

  @latest = Dir.glob("_links/*.md").max_by {|f| File.mtime(f)}
  puts "Latest link: \"#{@latest}\"\n"
  File.delete(@latest) if File.exist?(@latest)
  puts 'Link deleted'.green

end

task :default do

end
