platform :ios, '8.0'
source 'https://github.com/CocoaPods/Specs.git'
use_frameworks!

def common
    pod 'RxSwift',    '~> 3.2'
    pod 'RxCocoa',    '~> 3.2'
end

target 'Example' do
    common
    pod 'RxMapKit', :path => './'
end

post_install do |installer|
  installer.pods_project.targets.each do |target|
    target.build_configurations.each do |config|
        config.build_settings['SWIFT_VERSION'] = '3.0'
        #config.build_settings['MACOSX_DEPLOYMENT_TARGET'] = '10.10'
    end
  end
end
