function CMMRM_WaypointModel(data, routeModel) {
	this.data = data;
	this.routeModel = routeModel;
}

CMMRM_WaypointModel.prototype.getLat = function() {
	return this.data[0];
};

CMMRM_WaypointModel.prototype.getLng = function() {
	return this.data[1];
};

CMMRM_WaypointModel.prototype.getPosition = function() {
	return [this.getLat(), this.getLng()];
};

CMMRM_WaypointModel.prototype.getGoogleLatLng = function() {
	return new google.maps.LatLng(this.getLat(), this.getLng());
};

CMMRM_WaypointModel.prototype.setPosition = function(lat, lng) {
	this.data[0] = lat;
	this.data[1] = lng;
	jQuery(this).trigger('WaypointModel:setPosition', {lat: lat, lng: lng});
	return this;
};

CMMRM_WaypointModel.prototype.remove = function() {
	jQuery(this).trigger('WaypointModel:remove');
};

CMMRM_WaypointModel.prototype.getRoute = function() {
	return this.routeModel;
};