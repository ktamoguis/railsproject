First commit


routes:

get '/login' => 'sessions#new'
post '/login'  => 'sessions#create'
post '/logout' => 'sessions#destroy'


<%= form_for @user, url: ‘/login’ do |f| %>
  <label>Name:</label>
  <%= f.collection_select :name, User.all, :id, :name %>
  <label>Password:</label>
  <%= f.password_field :password %>
  <%= f.submit "Sign In" %>
<% end %>
