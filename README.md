# fullcode
def walk(start)
Dir.foreach(start) do |x|
path=File.join(start,x)
if x=="." or x==".."
print" "
next
elsif File.file?(path)
puts"/"+ path 
elsif File.directory?(path)
puts"/"+ path
walk(path) 
end 
end
end
walk("E:/asha")
