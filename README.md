

##Quick SnapKit example:

###NSLayoutConstraint
```Swift
profileImageView.translatesAutoresizingMaskIntoConstraints = false
profileNameLabel.translatesAutoresizingMaskIntoConstraints = false

profileImageView.leftAnchor.constraint(equalTo: profileImageView.superview.leftAnchor, constant: 16).isActive = true
profileImageView.widthAnchor.constraint(equalTo: profileImageView.heightAnchor).isActive = true
profileImageView.heightAnchor.constraint(equalToConstant: 50).isActive = true
profileImageView.centerYAnchor.constraint(equalTo: profileImageView.superview.centerYAnchor).isActive = true

profileImageView.rightAnchor.constraint(equalTo: profileNameLabel.leftAnchor, constant: -16).isActive = true

profileNameLabel.rightAnchor.constraint(equalTo: profileNameLabel.superview.rightAnchor, constant: 8).isActive = true
profileNameLabel.centerYAnchor.constraint(equalTo: profileNameLabel.superview.centerYAnchor).isActive = true
```

###SnapKit
```Swift
profileImageView.snp.makeConstraints{ make in

    make.left.equalToSuperview().offset(16)
    make.right.equalTo(profileNameLabel.snp.left).offset(-16)

    make.width.equalTo(profileImageView.snp.height)
    make.height.equalTo(50)

    make.centerY.equalToSuperview()

}

profileNameLabel.snp.makeConstraints{ make in

    make.right.equalToSuperview().offset(8)

    make.centerY.equalToSuperview()
}
```
