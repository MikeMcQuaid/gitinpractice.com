ENV["GUARD_NOTIFY"] = "false"

guard "jekyll-plus", serve: true do
  watch /.*/
  ignore /^_site/
end

guard "livereload" do
  watch %r{_site/.+\.(css|js|html|jpg|png)$}
end
