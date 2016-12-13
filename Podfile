
platform :ios, '9.0'
use_frameworks!

def pods
    pod 'AsyncDisplayKit'
    pod 'Appsee'
    pod 'DeviceUtil'
    pod 'FXBlurView'
    pod 'TPKeyboardAvoiding'
    pod 'pop'
    pod 'JPush', '~> 2.1.9'
    pod 'Fabric'
    pod 'RxSwift',    '~> 3.0'
    pod 'RxCocoa',    '~> 3.0'
    pod 'Reveal-SDK', :configurations => ['Debug']
end

target 'Positano' do
    swift_version = '3.0'

    pods

    target 'PositanoTests' do
        inherit! :search_paths
        pod 'RxBlocking', '~> 3.0'
        pod 'RxTest',     '~> 3.0'
    end
end

target 'PositanoKit' do
    pod 'RealmSwift'
end

post_install do |installer|
  installer.pods_project.targets.each do |target|
    target.build_configurations.each do |config|
      config.build_settings['SWIFT_VERSION'] = '3.0'
    end
  end
end
