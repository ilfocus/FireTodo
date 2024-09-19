source 'https://cdn.cocoapods.org/'
platform :ios, '13.0'

inhibit_all_warnings!

# Tools
pod 'SwiftFormat/CLI', '~> 0.40.0'
pod 'SwiftLint', '~> 0.35.0'

target 'FireTodo' do
  use_frameworks!
  # Firebase
  pod 'Firebase/Core', '~> 6.9'
  pod 'Firebase/Auth'
  pod 'Firebase/Firestore'
  pod 'FireSnapshot', '~> 0.6'

  # ReSwift
  pod 'ReSwift', '~> 5.0'
  pod 'ReSwiftThunk', '~> 1.2'
end

post_install do |installer|
  installer.generated_projects.each do |project|
    project.targets.each do |target|
      target.build_configurations.each do |config|
        config.build_settings['IPHONEOS_DEPLOYMENT_TARGET'] = '13.0'
      end
    end
  end
end
