require "rake"
require "rake/clean"

CLEAN.include FileList["_site"]

task default: :test

task :jekyll do
  sh "jekyll", "build"
end

desc "Run html proofer to validate the HTML output."
task test: :jekyll do
  require "html-proofer"
  HTMLProofer.check_directory(
    "./_site",
    check_external_hash: true,
    check_opengraph: true,
    check_html: true,
    check_img_http: true,
    only_4xx: true,
    parallel: { in_processes: 4 },
  ).run
end
