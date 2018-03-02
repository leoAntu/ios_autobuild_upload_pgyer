
#指定项目的scheme名称
scheme="CashLoan"
#蒲公英api_key和user_key
api_key="a2c30726504236ee68d7f85a318f7bf9"
user_key="48885f0e01f4211f219d03754434ac04"

default_platform(:ios)
platform :ios do
  desc "Push a new beta build to TestFlight"

     lane :test do
    	gym(
        	output_name: "#{scheme}",
        	silent: true,
        	clean: true,
		# Debug 和 Release
        	configuration: "Debug",
       	 	buildlog_path: "./fastlanelog",
		#指定打包所使用的输出方式，目前支持app-store, package, ad-hoc, enterprise, development, 和developer-id，即xcodebuild的method参数
        	export_method: "ad-hoc",
        	output_directory: "/Users/dingdongqianbaofuyin/Desktop/ipa/"
  	   )
         puts "开始上传蒲公英"
          # 开始上传蒲公英
          pgyer(api_key: “#{api_key}”, user_key: “#{user_key}”)
      end
end
