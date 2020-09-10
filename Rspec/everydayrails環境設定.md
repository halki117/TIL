# Rspecの実行
  $ bundle exec rspec
  ※実行箇所を指定したい場合(例えば spec/models/user_spec.rb とういファイルが存在した場合)
  $ bundle exec rspec spec/models/user_spec.rb




valid?を事前に行うと、errors.messagesにエラーの値が格納される。(テスト成功）
```
RSpec.describe Patient, type: :model do
    it 'is invalid without a name' do
        ho = Hoge.new()
        ho.valid? 
        expect(ho.errors.messages[:name]).to include('Can not be blank')
    end
end
```
